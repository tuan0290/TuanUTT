# Learn_Git
1.What is Git, GitHub, Bitbucket, Gitlab
- GIT
	- Version control system (VCS)
		- Hệ Thống Quản Lý Phiên Bản Tập Trung (Centralized Version Control Systems - CVCSs
			- Chứa một database đơn giản
			- Lưu lại mọi sự thay đổi của file, thư mục
			- Đây là một hệ thống quản lý phiên bản tập chung
			- Server sẽ lưu trữ tất cẩ các version của file và list các client có quyền thay đổi file trên server
		
		<p align="center">
  <img src="https://images.viblo.asia/full/cd075a32-c136-4b45-a72a-73be8d361b0d.png" width="350" title="hover text">
</p>
			- Nhược điểm khi Server bị dừng sẽ khồn thể kết nối. Dễ gây sự cố mất tài liệu
	
		-  Hệ Thống Quản Lý Phiên Bản Phân Tán - (Distributed Version Control Systems - DVCSs)
			- Về cơ bản giống với CVCS nhưng ở đây các máy khách sao chép toàn bộ repository về máy Điều này có nghĩa là khi Server bị ngắt, các máy khách vẫn làm việc bình thường trên Database ở máy trạm, sau đó commit (chuyển) lên Server sau, hoặc Database ở Server bị lỗi thì máy khách bất kỳ đều cỏ thể phục hồi lại cho Server

               <p align="center">
  <img src="https://images.viblo.asia/full/de65aef9-236b-46e8-845e-6bbbf22e9d64.png">
</p>


	- Git chính là hệ thống quản lý phiên bản phân tán (DVCS), với các ưu điểm: tốc độ, đơn giản, phân tán, phù hợp với dự án lớn nhỏ.


