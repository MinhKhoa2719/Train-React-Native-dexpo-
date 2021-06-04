# Train-React-Native
### Sơ lược về React Native
- React Native là một JavaScript Framework để xây dựng các ứng dụng di động gốc, sử dụng Mô-đun gốc và thành phần gốc để cải thiện hiệu suất ứng dụng
- Có thể sử dụng cùng một triển khai để triển khai trên cả nền tảng iOS và Android
### Về Expo
- Expo là một chuỗi công cụ mã nguồn mở và miễn phí được xây dựng React Native giúp xây dựng các dự án iOS và Android gốc bằng cách sử dụng JavaScript và React.
### Nếu đã cài đặt Nodejs thì ta dùng lệnh sau để cài đặt Expo về:
```jsx
npm install -g expo-cli
```
![image](https://user-images.githubusercontent.com/54676091/120816824-51dcb480-c57b-11eb-9037-6194a0549096.png)

### Bây giờ ta đã có thể dùng expo init để tạo dự án React Native mới
- Sử dụng lệnh để tạo
```jsx 
expo init helloWorld
```
![image](https://user-images.githubusercontent.com/54676091/120817507-fb23aa80-c57b-11eb-9707-27dce01938fa.png)

![image](https://user-images.githubusercontent.com/54676091/120817821-3a51fb80-c57c-11eb-8ac8-99a34410f45a.png)
-Nếu muốn trang có điều hướng thì chọn TAB..nếu không thì thôi

Để khởi động máy chủ, hãy cd đến thư mục và thực thi lệnh npm start.:
```jsx 
cd helloWorld 
npm start
```
## Kết quả 

![image](https://user-images.githubusercontent.com/54676091/120818582-f4496780-c57c-11eb-8081-a2b3bc519351.png)

![image](https://user-images.githubusercontent.com/54676091/120818680-075c3780-c57d-11eb-9b84-3346b74fda26.png)

## Cách chạy trên thiết bị thực tế
#### Tải xuống ứng dụng Expo từ Google Play Store hoặc App Store 
#### Điều quan trọng tiếp theo là đảm bảo điện thoại di động được kết nối cùng một Mạng với máy tính.
- Ta sẽ tiếp tục làm như sau:
Mở Expo và quét mã QR trong thiết bị đầu cuối hoặc trình duyệt của bạn
  

## Hello World
Nhìn vào tệp App.js
Giờ xóa hết trong App.js và thêm code mới vào để có thể hiện ra Hello World
##### hãy nhớ dòng quan trọng : import Button from ‘react-native’
Thêm code :
```jsx
export default class App extends React.Component {
   constructor(props){
     super(props);
     this.state = {
     name: 'World!',
     }
   }
   onClick = () => {
     this.setState({
     name: 'John!',
     })
   };
   render() {
   return (
     <View style={styles.container}>
       <Text>Hello {this.state.name}</Text>
       <Button 
            onPress={() => {this.onClick()}} 
            title='Click me'
            color='#4169E1'>
       </Button>
     </View>
   );
   }
}
const styles = StyleSheet.create({
   container: {
     flex: 1,
     backgroundColor: '#fff',
     alignItems: 'center',
     justifyContent: 'center',
   }, 
   nameText: {
     fontSize: 50,
     padding: 15,
   }
});
```

- Trong đoạn mã trên, "Text" sẽ hiển thị tên ở trạng thái. Giá trị ban đầu của "name" là "World!" và nhấn nút "Click me" sẽ gọi hàm "onClick" thay đổi giá trị "name" thành World! .

- Khi nói đến Button, React Native cung cấp các tùy chọn rất hạn chế cho thành phần đó. Thành phần nút hiển thị nút gốc trên nền tảng. Bởi vì điều này, nó không có nhiều style
- Vì vậy, để thay đổi màu của nút, chuyển màu # 4169E1 thành màu prop.
- Muốn kiểm soát nhiều hơn về ngoại hình, hãy sử dụng TouchableOpacity thay vì nút.


## Kết Quả

![image](https://user-images.githubusercontent.com/54676091/120830224-7b500d00-c588-11eb-966c-3e1a736e2346.png)




Lưu ý:
nhớ import button

![image](https://user-images.githubusercontent.com/54676091/120829936-2dd3a000-c588-11eb-9ab8-aea26f7076da.png)



