# ANOMALY DETECTION

Dự án này ứng dụng mô hình học sâu Autoencoder để phát hiện các hành vi bất thường trong hệ thống, từ đó dự báo nguy cơ rò rỉ dữ liệu (Data Breach). Bằng cách học cách tái tạo (reconstruct) các dữ liệu bình thường, mô hình có thể xác định các điểm dữ liệu lạ (anomalies) dựa trên sai số tái tạo cao.

📌 Tổng quan dự án
Rò rỉ dữ liệu thường bắt đầu từ những truy cập bất thường hoặc lưu lượng mạng không xác định. Dự án này tập trung vào:
Phân tích hành vi người dùng/hệ thống qua các đặc trưng (features).
Sử dụng kiến trúc mạng thần kinh không giám sát (Unsupervised Learning).
Thiết lập ngưỡng (threshold) để cảnh báo sớm các dấu hiệu xâm nhập.

🏗 Kiến trúc mô hình
Mô hình Autoencoder bao gồm hai phần chính:
Encoder: Nén dữ liệu đầu vào thành một biểu diễn không gian thấp chiều (Latent Space).
Decoder: Khôi phục dữ liệu ban đầu từ không gian nén đó.
Khi dữ liệu "bất thường" đi qua mạng đã được huấn luyện với dữ liệu "bình thường", khả năng tái tạo của Decoder sẽ kém đi, dẫn đến Reconstruction Error lớn — đây chính là tín hiệu để phát hiện rò rỉ.

🚀 Công nghệ sử dụng
Ngôn ngữ: Python
Thư viện AI/ML: TensorFlow/Keras hoặc PyTorch, Scikit-learn
Xử lý dữ liệu: Pandas, Numpy
Trực quan hóa: Matplotlib, Seaborn

🛠 Cài đặt và Sử dụng
### Clone repository:
git clone https://github.com/Quanggatay2005/anomaly_detection.git
cd anomaly_detection
### Cài đặt môi trường:
pip install -r requirements.txt
Tải bộ dữ liệu và đưa 2 file thứ Hai và thứ năm vào cùng 1 folder: https://cicresearch.ca/CICDataset/CIC-IDS-2017/browse.php?p=CIC-IDS-2017%2FCSVs

### Huấn luyện mô hình: 
chạy file main.ipynb

