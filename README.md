# DL Playground

Thư mục dùng để lưu các notebook thử nghiệm, bài tập và đoạn code nhanh trong quá trình học Deep Learning.

## Bắt đầu nhanh với Google Colab

1. Mở [Google Colab](https://colab.research.google.com/).
2. Chọn **File > Upload notebook** và tải file `dl_playground_template.ipynb`.
3. Chọn **Runtime > Change runtime type**:
   - **Hardware accelerator**: chọn **T4 GPU** nếu cần chạy mô hình.
   - **Runtime shape**: giữ mặc định nếu chỉ thử code nhỏ.
4. Chạy lần lượt các cell từ trên xuống bằng nút ▶ hoặc **Runtime > Run all**.

## Kết nối Google Drive

Trong notebook, chạy cell kết nối Drive. Colab sẽ yêu cầu:

1. Cho phép truy cập tài khoản Google.
2. Chọn tài khoản muốn dùng.
3. Sao chép mã xác thực nếu được yêu cầu và dán lại vào Colab.

Sau khi kết nối, file trong Drive có thể được truy cập qua:

```python
/content/drive/MyDrive/
```

Nên tạo một thư mục riêng, ví dụ:

```text
MyDrive/dl-playground/
├── data/
├── notebooks/
├── models/
└── outputs/
```

## Mở notebook trực tiếp từ GitHub

Nếu repository đã được push lên GitHub, thay `OWNER/REPO` và `BRANCH` trong URL sau:

```text
https://colab.research.google.com/github/OWNER/REPO/blob/BRANCH/dl_playground_template.ipynb
```

Trong Colab, chọn **File > Save a copy in Drive** để lưu bản làm việc vào Google Drive.

## Chạy local

Nếu đã cài Python và Jupyter:

```powershell
py -m pip install jupyterlab notebook
py -m jupyter lab
```

Sau đó mở file notebook trong trình duyệt. Các cell dành riêng cho Colab sẽ tự bỏ qua nếu đang chạy local.

## Quy ước sử dụng

- Mỗi chủ đề hoặc bài thử nghiệm nên có một notebook riêng.
- Đặt tên theo dạng `topic_experiment.ipynb`.
- Lưu dữ liệu lớn, model và output ở Drive; không commit vào Git.
- Ghi rõ nguồn dữ liệu, phiên bản thư viện và kết quả chính trong notebook.
