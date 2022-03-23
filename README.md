# Learn_Git
1.What is Git, GitHub, Bitbucket, Gitlab
- GIT
	- Version control system (VCS)
		- Hệ Thống Quản Lý Phiên Bản Tập Trung (Centralized Version Control Systems - CVCSs
			- Chứa một database đơn giản
			- Lưu lại mọi sự thay đổi của file, thư mục
			- Đây là một hệ thống quản lý phiên bản tập chung
			- Server sẽ lưu trữ tất cẩ các version của file và list các client có quyền thay đổi file trên server
			- <img src="https://images.viblo.asia/full/cd075a32-c136-4b45-a72a-73be8d361b0d.png" width="350" title="hover text">
			- Nhược điểm khi Server bị dừng sẽ khồn thể kết nối. Dễ gây sự cố mất tài liệu
			
		- HệThống Quản lý phiên bản Phân Tán (Distributed Version Control Systems - DVCSs)
			- Về cơ bản giống với CVCSs  nhưng các máy client sao chép toàn bộ repository trên server về local
			- Khi server bị ngắt máy khách vấn có thể làm việc bình thường trên database của máy client, sau đó có thể commit lên server sau.
			- Máy khách cũng có thể phục hồi lại cho server
			- <img src="https://images.viblo.asia/full/de65aef9-236b-46e8-845e-6bbbf22e9d64.png">
	- Git chính là hệ thống phiên bản phân tán (DVCs), với các ưu điểm về tốc độ, đơn giản, phân tán, phù hợp với dự án lớn nhỏ.

