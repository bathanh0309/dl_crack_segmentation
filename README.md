## Dùng Unet để phân vùng tọa độ vết nứt mặt đường
### Cấu trúc dữ liệu
- **Code**: Các notebook huấn luyện và kiểm thử mô hình.
- **Dataset (`data_cau1/`)**: Bộ dữ liệu ảnh vết nứt bê tông (đã chia folder train/test).
- **Model Checkpoint (`checkpoint_unet.pth`)**: Trọng số mô hình U-Net đã huấn luyện (được lưu trữ bằng Git LFS).
---

### Cách đẩy file Model lớn (>100MB)
GitHub giới hạn file thường là 100MB. Để upload model (ví dụ 355MB), cần dùng **Git LFS (Large File Storage)**.

```bash
# Cài đặt LFS (chỉ làm 1 lần)
git lfs install

# Theo dõi file model
git lfs track "*.pth"
git add .gitattributes

# Upload như bình thường
git add checkpoint_unet.pth
git commit -m "Upload model via LFS"
git push origin main
```
<img width="4470" height="2966" alt="training_history" src="https://github.com/user-attachments/assets/de19e2f7-d914-4022-8bd9-7b8d0599aa41" />

<img width="1462" height="1490" alt="image" src="https://github.com/user-attachments/assets/2e5eadc9-c5b1-4a94-b989-69596873985f" />

<p align="center">
  <img src="https://github.com/user-attachments/assets/a3ca19e1-7f30-4cd0-888b-d8e037163bfd"
       alt="Crack segmentation results"
       width="1400">
</p>

