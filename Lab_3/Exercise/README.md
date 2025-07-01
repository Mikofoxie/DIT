````markdown
# Xử Lý Ảnh Cơ Bản với OpenCV và Python

Dự án này là tập hợp các ví dụ thực hành về **xử lý ảnh cơ bản** sử dụng thư viện **OpenCV** kết hợp với **NumPy** và **Matplotlib**. Các thao tác được minh họa gồm: tịnh tiến, xoay, phóng to hình ảnh, xử lý vùng chọn (ROI), và một công cụ tương tác trong môi trường Jupyter Notebook.

## 🧰 Yêu cầu cài đặt

Bạn cần cài đặt các thư viện sau trước khi chạy các script:

```bash
pip install opencv-python numpy matplotlib ipywidgets jupyterlab
````


## 🧪 Mô tả từng script

### 1. Tịnh tiến đối tượng – `01_translation.py`

* Ảnh sử dụng: `colorful-ripe-tropical-fruits.jpg`
* Nội dung:

  * Cắt quả kiwi từ ảnh.
  * Tô đen vùng cũ.
  * Dán kiwi vào vị trí mới (dịch phải 30px).
  * Vẽ khung hình chữ nhật cho cả vị trí cũ và mới.

---

### 2. Chỉnh sửa vùng ảnh (ROI) – `02_roi_manipulation.py`

* Ảnh sử dụng: `colorful-ripe-tropical-fruits.jpg`
* Nội dung:

  * Cắt vùng chứa đu đủ và dưa hấu.
  * Thay màu đu đủ thành **xanh lá**.
  * Thay màu dưa hấu thành **hồng cánh sen**.

---

### 3. Xoay đối tượng – `03_rotation.py`

* Ảnh sử dụng: `quang_ninh.jpg`
* Nội dung:

  * Cắt vùng chứa ngọn núi và con thuyền.
  * Xoay mỗi vùng một góc **45 độ** bằng `cv2.getRotationMatrix2D`.

---

### 4. Phóng to ảnh – `04_scaling.py`

* Ảnh sử dụng: `pagoda.jpg`
* Nội dung:

  * Cắt vùng chứa ngôi chùa.
  * Phóng to **5 lần** bằng `cv2.resize()` với nội suy `INTER_CUBIC`.

---

### 5. Công cụ xử lý ảnh tương tác – `05_interactive_tool.ipynb`

* Chạy trong **Jupyter Notebook/Lab**.
* Tính năng:

  * Chọn ảnh đầu vào.
  * Chọn hành động: *tịnh tiến*, *xoay*, *phóng to*, *thu nhỏ*.
  * **Bản đồ tọa độ**: click vào ảnh để xem (x, y) – hỗ trợ chọn ROI cho các script khác.

---


## 📸 Kết quả minh họa

Từng script sẽ hiển thị kết quả trực quan bằng `matplotlib`. Một số script còn lưu ảnh kết quả như `mountain_rotated.jpg`, `pagoda_scaled_5x.jpg`, v.v.