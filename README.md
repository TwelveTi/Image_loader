ID: 22110083.

NAME: Phan Dinh Trung

Image Loader App
React Native - Ứng Dụng Tải Ảnh Đơn Giản

Mô tả: Một ứng dụng Android cơ bản được xây dựng bằng React Native, cho phép người dùng nhập URL hình ảnh và hiển thị ảnh đó trong giao diện ứng dụng. Dự án này minh họa cách sử dụng AsyncTask, AsyncTaskLoader, kiểm tra trạng thái mạng, broadcast receiver và thông báo từ dịch vụ nền.

Mục tiêu:

Tạo một ứng dụng React Native có thể:

Tải ảnh từ URL do người dùng nhập

Sử dụng AsyncTask hoặc AsyncTaskLoader (tương đương async/await trong React Native)

Kiểm tra kết nối Internet bằng NetInfo

Sử dụng broadcast receiver để theo dõi thay đổi kết nối mạng

Hiển thị thông báo từ background service định kỳ bằng react-native-push-notification

Tính năng chính:

Tải ảnh:

Người dùng nhập URL vào ô nhập liệu

Nhấn nút "Load Image" để tải ảnh

Hiển thị ActivityIndicator khi đang tải

Thông báo trạng thái thành công hoặc lỗi

Kiểm tra kết nối mạng:

Sử dụng @react-native-community/netinfo để theo dõi kết nối

Nếu không có Internet, nút "Load Image" bị vô hiệu hóa

Hiển thị thông báo “No internet connection” khi mất mạng

Gửi thông báo định kỳ:

Cứ mỗi 5 phút, ứng dụng gửi một local notification: "Image Loader Service is running"

Thiết lập thông báo qua channel trên Android

Công nghệ sử dụng:

React Native

JavaScript hoặc TypeScript

NetInfo để kiểm tra kết nối mạng

PushNotification để gửi thông báo nền

Quy trình hoạt động:

Người dùng nhập URL ảnh

Ứng dụng kiểm tra kết nối mạng bằng NetInfo

Nếu offline, nút bị vô hiệu hóa và hiển thị thông báo mất mạng

Khi nhấn Load Image, ứng dụng gọi fetch() để tải ảnh

Hiển thị biểu tượng đang tải

Hiển thị ảnh nếu thành công hoặc lỗi nếu thất bại

Mỗi 5 phút, hiển thị thông báo: "📸 Image Loader Service is running"

Quyền cần thiết trong AndroidManifest.xml:
``
<uses-permission android:name="android.permission.INTERNET" /> 
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
``
