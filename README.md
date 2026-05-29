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
