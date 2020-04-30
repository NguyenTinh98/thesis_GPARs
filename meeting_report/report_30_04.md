# Nội dung họp ngày 30/04/2020

## Cập nhật một số cấu trúc tổ chức.
- **Class Edge:**
	+ Điểm đầu: u
	+ Điểm cuối: v
- **Class Node:**
	+ Thuộc tính:
		+ ID
    + Danh sách các node có liên kết: Kiểu list.
		+ Danh sách các thuộc tính: Kiểu List - kích thước được xác định trước (là số lượng thuộc tính cần thiết - thuộc tính nào không có dữ liệu, được set là null).
    --- Danh sách các thuộc tính: Để trong class node hay đưa ra ngoài class Graph ???
- **Class Graph:**
	+ Thuộc tính:
		+ Danh sách các cạnh (edge): kiểu List - mỗi phần tử là 1 object kiểu **Edge**
		+ Danh sách các đỉnh (node): kiểu List - mỗi phần tử là 1 object kiểu **Node**
- **Class Site:**
		+ Thuộc tính:
			+ Danh sách các Graph: Kiểu List - mỗi phần tử là 1 object kiểu **Graph**
			+ Danh sách các CrossingEdge: Kiểu List - mỗi phần tử là 1 object kiểu **Edge**
			+ Danh sách các VirtualNode: kiểu List - mỗi phần tử là 1 object kiểu **Node*
     
 ## Một vài vấn đề khác:
 - Hardware để thực hiện trên dữ liệu lớn.
 - Compare kết quả với các thuật toán khác: mã nguồn, hardware, tiêu chí ??
 - Kiểm nghiệm độ chính xác, thời gian chạy của thuật toán tự cài ??
