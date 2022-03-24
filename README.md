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

2.How to install git command on clients (Windows, Linux)
- Windows
	- https://git-scm.com/downloads
- Ubuntu
	- sudo apt update
	- sudo apt install git -y
	- git --version
- CentOS
	- sudo yum check-update
	- sudo yum install git -y
	- git --version

3.Git concepts
- Repository: kho chứa bao gồm source code và lịch sử thay đổi, cũng như nộ dung của từng file và từng cá nhân đóng gióp
- Local repository: Kho lưu trữ tại máy client
- Remote repository: Kho lưu trữ trên server 
- Git add: sử dụng cho việc đưa những thay file đã được cập nhật tại một thời điểm quan trọng hoặc hoàn thành lên môi trường Std.
- Git rm: về cơ bản có hể hiểu là xóa file trên stg và working dir
	- Xóa trên stg và working dir: sau khi add và commmit sử dụng "git rm <tên file>" hoặc "git rm -r ."
	- Chỉ xóa trên stg: "git rm --cache <tên file>" kiểm tra trên stg "git ls-file" sẽ thấy file đã mất nhưng trên local vẫn còn
	- chỉ xóa trên working dir: rm -f <tên file>
- Git commt: Thực hiện việc đưa các fle đã được thay đổi lên local repository với việc lưu trữ theo commit 
- Git pull: là sự kết hợp của fetch và merge
	- git fetch lấy tất cả lịch sử hay đổi của một nhánh rên repo được track
	- gii merge sẽ hợp nhất nhánh hiện tại với một nhánh được chỉ định
- Git dif: dùng để so sánh các thay đổi các commit hoặc thay đổi trên remote và local
- Git Checkout : dùng để chuyển nhánh hoặc tạo nhánh mới từ nhánh hiện tại
- Git rebase: dùng để gộp commit(-i) hoặc gộp một nhánh đang đứng vào nhánh được chỉđịnh
 
