# Platform Policy Skills

Bộ skill cho Codex để rà soát sản phẩm, video và kênh trước khi đăng hoặc khi đã có cảnh báo. Mỗi phát hiện gắn với bằng chứng cụ thể, điều khoản chính thức và cách sửa.

## Cài đặt

```powershell
npx skills@latest add LucentDinh/platform-policy-skills
```

Xem danh sách trước khi cài:

```powershell
npx skills@latest add LucentDinh/platform-policy-skills --list
```

Cài cả bộ vào dự án hiện tại cho Codex:

```powershell
npx skills@latest add LucentDinh/platform-policy-skills --skill '*' --agent codex --yes --copy
```

Thêm `--global` nếu muốn cài cho tài khoản người dùng và gọi từ nhiều dự án. Nếu CLI báo không tìm thấy skill, chạy lại lệnh `--list` với đúng tên repo hoặc dùng đường dẫn tới bản clone để kiểm tra cục bộ.

## Chọn skill

| Skill | Phạm vi | Ví dụ |
| --- | --- | --- |
| [`youtube-policy-audit`](skills/youtube-policy-audit/SKILL.md) | Video, Shorts, kênh YouTube và nội dung tài trợ | `$youtube-policy-audit Rà kênh này trước khi nộp YPP. Đây là link kênh và các video mẫu.` |
| [`tiktok-policy-audit`](skills/tiktok-policy-audit/SKILL.md) | Video, hồ sơ TikTok và nội dung thương mại | `$tiktok-policy-audit Rà video và caption này, kiểm cả nhãn AI và khai báo quảng bá.` |
| [`tiktok-shop-policy-audit`](skills/tiktok-shop-policy-audit/SKILL.md) | Sản phẩm, bài đăng bán, video gắn sản phẩm và LIVE | `$tiktok-shop-policy-audit Kiểm listing và kịch bản affiliate này cho thị trường Việt Nam.` |

Với video tạo bằng MoneyPrinterTurbo, Remotion hoặc ViMax, gửi bản MP4, kịch bản hoặc transcript, tiêu đề, thumbnail, caption và thông tin nguồn nhạc, footage, ảnh hoặc giọng nói mà bạn có. Với kênh, gửi link và vài bài đại diện. Thông báo từ Studio giúp kiểm tra các hạn chế mà tài khoản đang gặp.

Skill có thể chạy khi chỉ có một phần đầu vào. Báo cáo ghi phạm vi đã xem và đánh dấu phần cần thêm dữ liệu. Mỗi lần rà soát, đối chiếu nguồn chính thức đang áp dụng cho thị trường và loại nội dung. Nền tảng quyết định việc gỡ nội dung, duyệt sản phẩm và kiếm tiền.

## Kiểm tra bản clone

Từ gốc repo, chạy `npx skills@latest add . --list` để kiểm tra CLI nhận đủ ba thư mục trong `skills/`. Có thể cài bản clone vào một thư mục thử nghiệm bằng cách thay tên repo trong lệnh cài bằng đường dẫn tuyệt đối tới bản clone.

Giấy phép [MIT](LICENSE).
