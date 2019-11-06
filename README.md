## 0.Display
![screenshot](src/main/resources/static/team31Backend.jpg)
### 사용자의 위치를 자동으로 추적하여 화면에 데이터를 나타냄.
> 추가한 라이브러리 목록
1. import { Alert } from "react-native";
2. import * as Location from "expo-location";
3. import axios from "axios";

### 기존 nomad code는 현재위치, 현재기온, title, substitle 구현
### 추가로 temp_min, temp_max, 현재위치표시 및 국가 구현
> const {
      data: {
        main: { temp,temp_min,temp_max },
        weather,
        name,
        sys:{country}

      }
      
>render() {
    const { isLoading, temp, condition, place,con, temp_max, temp_min} = this.state;
    return isLoading ? (
      <Loading />
    ) : (
      <Weather temp={Math.round(temp)} condition={condition} place={place} con={con}
      temp_max={Math.round(temp_max)} temp_min={Math.round(temp_min)}/>
    );
  }





