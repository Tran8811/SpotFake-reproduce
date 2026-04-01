### Multimodal Fake News Detection: SpotFake & SpotFake+ Reproduction
Tái hiện reproduction và tối ưu hóa hai mô hình phát hiện tin giả đa phương thức: 
SpotFake (2019) https://github.com/shiivangii/SpotFake 
SpotFake+ (2020) https://github.com/shiivangii/SpotFakePlus.git 

### Kiến trúc Mô hình
1. SpotFake (Cho bài đăng mạng xã hội ngắn)
Text Branch: bert-base-chinese (Hỗ trợ tiếng Trung cho tập Weibo).

Image Branch: VGG19 (Pre-trained trên ImageNet).

Fusion: Late Fusion thông qua các lớp Dense, ReLU và Dropout.

Framework: PyTorch.

2. SpotFake+ (Cho bài báo dài)
Text Branch: xlnet-base-cased.

Image Branch: VGG19.

Fusion: Concatenate đặc trưng 100-chiều của ảnh và chữ -> 200-chiều Multimodal Vector -> Classification.

Framework: Keras / TensorFlow.

### Bộ dữ liệu 

PolitiFact (FakeNewsNet): Các bài báo chính trị tiếng Anh.

GossipCop (FakeNewsNet): Các bài báo giải trí tiếng Anh (Dữ liệu lớn, độ mất cân bằng cao).

Weibo: Các bài đăng tiếng Trung trên mạng xã hội Weibo.
