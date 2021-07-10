#Cách chia component trong Reactjs

#Hai loại component
- **Container**: Smart component
    - Quản lý, xử lý dữ liệu
    - Không quan tâm render UI ntn
    - Chỉ quan tâm render cái gì
    - Có thể chưa container con và các components

- **Component** Dumb component
    - Cho gì render đó.
    - Không biết dữ liệu đến từ đâu.
    - Thường chỉ có props, Không có state.
    - Tái sử dụng, với props khác nhau, Render khách




#ReactJS: PrpOs, State or Global State

Props 
- Không thay đổi được
- Được truyền từ component cha
- Tạo sự đa dạng cho components
```
function Box(props){
    return(
        <div
            style= {{background: props.color}}
        ></div>
    )
}

funtion App(){
    return (
        <div>
            <Box color="deeppink">
            <Box color="green">
        </div>
    )
}


State
- Thay đổi được
- Dùng khi chỉ được sử dụng cới * Một * components hiện tại
- Ví dụ: 
  - Dữ liệu từ API chỉ dùng trong component.
  - CurrentSend trong count down
  - ...

Global State (Redux)
- Thay đổi được
- Nếu được dùng bởi * Nhiều * components
- Ví dụ:
    - Thông tin logged in user
    - Thông tin của giỏ hàng
    - ..

## Demo
- ColorBox
    - Props: color
    - State: N/A
    - Render: a box with background color is props.color
- Countdown
    - Props: seconds
    - State: currentSecond
    - Handle to update currentSecond per second.
    - Render: currentSecond value.
## TAKEWAY
- Props thì được truyền từ components cha.
- State thì dùng một components.
- Global State nếu dùng cho nhiều components