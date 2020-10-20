# thesis_GPARs
## References
- http://simpledatamining.blogspot.com/2015/03/graph-pattern-mining-gspan-introduction.html
- https://hpi.de/mueller/lehre/aktuelle-vorlesung/ws-1617/graph-mining.html?fbclid=IwAR3ikZEdPa5jKAEn1Iubca3b0stOx-0TrYy2gkIdqzEL4uwVNuEKfmUYPe8
- https://github.com/ehab-abdelhamid/GraMi

## Thư mục SOURCE:
- DATASETS: chứa các tập dữ liệu của nhóm. 
  - Bao gồm 5 thư mục con chứa 5 tập dữ liệu: cora, CL_10k_1d8_L5, SW_10000_6_0d3_L5, GenTest1, GenTest2.
  - Mỗi thư mục gồm 2 file: *_profiles.txt (thông tin của các đỉnh) và *_relationships.txt (các cạnh trong đồ thị).
    + Main.ipynb: file mã nguồn chính.
    + Thesis_Undirected_GPAR_Final.ipynb: file mã nguồn chứa cài đặt của các class, hàm cho đồ thị vô hướng.
    + Thesis_Directed_GPAR_Final.ipynb: file mã nguồn chứa cài đặt của các class, hàm cho đồ thị có hướng.
    + Thesis_Measure.ipynb: file mã nguồn chứa các cài đặt liên quan đến thực nghiệm.

## Hướng dẫn thực thi mã nguồn.
- File mã nguồn chính gồm 3 file Main.ipynb, Thesis_Directed_GPAR_Final.ipynb và Thesis_Undirected_GPAR_Final.ipynb.
- Chương trình chính trong file Main.ipynb. Thực hiện các bước sau để thực thi mã nguồn trong file Main.ipynb:
	- Setup: Run tất cả các cell trong phần 'Setup Environment' để import các thư viện và module cần thiết từ 2 file Thesis_Directed_GPAR_Final.ipynb và Thesis_Undirected_GPAR_Final.ipynb (Bỏ qua các cell mount đến GoogleDrive nếu không cần thiết).
  	- Khai thác tập phổ biến:
		+ Thực thi hàm FPMiner(profiles_data, relationships_data, minsup, directed_=True) để khai thác các mẫu đồ thị con phổ biến.
			+ Input:
				+ profiles_data: [đường dẫn] file chứa thông tin profile của đồ thị (chứa thông tin các đỉnh).
				+ relationships_data: [đường dẫn] file chứa thông tin các cạnh trong đồ thị.
				+ minsup: Ngưỡng hỗ trợ tối thiểu của các mẫu đồ thị muốn khai thác.
				+ directed: Áp dụng thuật toán có hướng hay vô hướng (mặc định là True - có hướng).
			+ Output: Các mẫu đồ thị con phổ biến
   	- Khai thác luật kết hợp:
		+ Thực thi hàm ruleGen(fp, conf=0.9) để khai thác luật từ các mẫu đồ thị phổ biến.
			+ Input:
				+ fp: Các mẫu đồ thị được khai thác ở bước khai thác tập phổ biến (Output của hàm FPMiner).
				+ conf: Ngưỡng tin cậy tối thiểu để sinh ra các luật.
			+ Output:
				+ rules: Các luật phổ biến (dạng List).
				+ confs: Độ tin cậy tương ứng của các luật rules được sinh ra (dạng List).

## Group's Gmail
- Gmail: thesis0820@gmail.com
- Password: n*\*n*\*9*
- Account Overleaf: the same as gmail.
