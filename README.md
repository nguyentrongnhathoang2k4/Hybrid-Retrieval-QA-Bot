# PTIT AI - RAG System (Hybrid Retrieval QA Bot)

Hệ thống hỏi đáp thông minh dựa trên tài liệu PDF sử dụng kiến trúc RAG (Retrieval-Augmented Generation). Dự án kết hợp phương thức tìm kiếm từ khóa (BM25) và tìm kiếm ngữ nghĩa (Dense dựa trên TF-IDF) thông qua thuật toán gộp thứ hạng RRF (Reciprocal Rank Fusion).

##  Tính Năng
* **Hybrid Retrieval:** Gộp kết quả của BM25 và Dense + Re-ranking tối ưu khả năng tìm kiếm ngữ cảnh chuẩn xác.
* **Evaluation Metrics:** Tích hợp bộ đo chuẩn hóa: Exact Match (EM), F1 Score, và Mean Reciprocal Rank (MRR).
* **Gradio UI:** Giao diện Chatbot trực quan, hỗ trợ hiển thị nguồn trích dẫn dữ liệu (Tên tệp, số trang) và điểm số đồng thời cho phép tải lên tài liệu mới trực tiếp từ giao diện.

##  Hướng dẫn chạy
1. Truy cập và mở file `RAG_NPL.ipynb` bằng Google Colab.
2. Thiết lập `GOOGLE_API_KEY` (Gemini API Key).
3. Upload tệp dữ liệu đánh giá `Dataset_Demo_3_Cau_Chien_Thuat.xlsx` và các file PDF tài liệu vào môi trường Colab.
4. Chạy tuần tự các bước để khởi chạy giao diện Gradio.
💻 Hướng Dẫn Khởi Chạy (Google Colab / Local)
Yêu cầu môi trường
Python 3.10+
Các thư viện cốt lõi: rank_bm25, langchain, google-generativeai, gradio, pandas, openpyxl.
Một Google Gemini API Key hợp lệ.
+Các bước thực hiện
Tải mã nguồn về máy hoặc import vào Colab:
git clone [https://github.com/nguyentrongnhathoang2k4/Hybrid-Retrieval-QA-Bot.git]
+Cài đặt các gói thư viện phụ thuộc:
pip install rank_bm25 langchain-community google-generativeai gradio pandas openpyxl pypdf
+Cấu hình API Key:
Thay thế hoặc thiết lập biến môi trường cho token của bạn:
GOOGLE_API_KEY = "Nhập_API_Key_Gemini_Của_Bạn_Tại_Đây"
+Chuẩn bị dữ liệu kiểm thử:
Đảm bảo tệp dữ liệu đánh giá Dataset_Demo_3_Cau_Chien_Thuat.xlsx và các tệp tài liệu PDF mẫu được đặt chung vào thư mục chạy (hoặc upload thẳng lên mục tệp của Google Colab).
+Chạy ứng dụng:
Thực thi tuần tự các cell trong file RAG_NPL.ipynb. Khi chạy đến bước cuối cùng, hệ thống sẽ trả về một đường dẫn Gradio (Local & Public URL). Hãy nhấp vào link đó để mở giao diện Chatbot.

📊 Kết Quả Đánh Giá Sơ Bộ
Hệ thống xử lý mượt mà các truy vấn phức tạp nhờ cơ chế Re-ranking của RRF.

Chỉ số MRR đạt mức cao, chứng minh các phân đoạn chứa câu trả lời chính xác đa số đều nằm ở top đầu của kết quả tìm kiếm.

👤 Thông Tin Dự Án
Tác giả: Nguyễn Trọng Nhật Hoàng (2004)

Đơn vị: Học viện Công nghệ Bưu chính Viễn thông (PTIT)

Môn học: Xử lý ngôn ngữ tự nhiên (NLP) / Hệ thống AI thông minh
