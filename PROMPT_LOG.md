# NHẬT KÝ PROMPT ENGINEERING (VIBE CODING LOG)
- **Họ và tên:** Phan Thị Ngọc Duyên
- **MSSV:** 426000035
- **Tên đề tài Website:** UI/UX Masterclass Landing Page
- **Công cụ AI đã sử dụng:** GitHub Copilot / VS Code Copilot (dựng bản đầu), Claude của Anthropic (nâng cấp hiệu ứng, kiểm tra và sửa mã)

## 1. Yêu cầu ban đầu (System/Initial Prompt)
# Role (Actor)
Bạn là một Senior Frontend Developer chuyên nghiệp, có kỹ năng thiết kế giao diện Landing Page hiện đại, tối ưu trải nghiệm người dùng (UX/UI) và thành thạo thuần thục HTML5, CSS3.

# Mục tiêu
Thiết kế một Landing Page sự kiện "Tech Workshop: UI/UX Design Masterclass" hoàn chỉnh, trực quan, đẹp mắt và tuân thủ tuyệt đối các ràng buộc kỹ thuật bên dưới.

# Yêu cầu kỹ thuật
1. **Công nghệ:** Chỉ sử dụng **HTML5** và **CSS3 (External CSS)**. **TUYỆT ĐỐI KHÔNG SỬ DỤNG JAVASCRIPT** hoặc các thư viện JS bên ngoài (Không dùng JS cho hiệu ứng cuộn trang).
2. **Hiệu ứng Animate.css:** Tích hợp thư viện Animate.css qua CDN để áp dụng hiệu ứng động (ví dụ: `fadeInDown`, `zoomIn`) cho các phần tử chính (Tiêu đề H1 ở Hero Section, nút CTA chính).
3. **Hiệu ứng :hover, :focus tùy chỉnh bằng CSS:**
   - Nút bấm (Buttons) và các thẻ bài viết (Cards): Viết hiệu ứng `:hover` nổi khối (`transform: translateY`), phóng to nhẹ, thay đổi màu sắc và đổ bóng (`box-shadow`).
   - Các ô nhập liệu (`input`, `textarea`) trong form: Viết hiệu ứng `:focus` đổi màu viền sáng nổi bật và tạo độ bóng mượt mà.
4. **Giao diện Responsive:** Thiết kế tương thích tốt trên cả máy tính (Desktop) và điện thoại (Mobile).

# Nội dung chi tiết của Landing Page (Tech Workshop: UI/UX Design Masterclass)

1. **Header / Navigation Bar:**
   - Logo/Tên sự kiện: `UI/UX Masterclass`
   - Menu links: Giới thiệu, Lợi ích, Diễn giả, Lịch trình.
   - Nút CTA: "Đăng ký ngay".

2. **Hero Section (Phần mở đầu):**
   - Tiêu đề chính (H1): *Chinh Phục UI/UX Design Trong Kỷ Nguyên Số* (Áp dụng hiệu ứng từ Animate.css).
   - Mô tả ngắn: Workshop thực chiến giúp bạn nắm vững tư duy thiết kế, làm chủ quy trình dựng wireframe và xây dựng sản phẩm số chuyên nghiệp.
   - Nút CTA chính: **"Đăng Ký Giữ Chỗ Ngay"** (Hiệu ứng `:hover` phóng to nhẹ và đổi màu).

3. **Benefits Section (Giá trị nhận được - Dạng Cards):**
   - Tiêu đề section: *Bạn sẽ nhận được gì từ sự kiện?*
   - Card 1: **Tư duy thiết kế** - Hiểu sâu về user-centric design và phương pháp nghiên cứu hành vi người dùng cốt lõi.
   - Card 2: **Thực hành thực tế** - Quy trình chuyển đổi ý tưởng thô thành giao diện trực quan trên Figma.
   - Card 3: **Chia sẻ độc quyền** - Bí quyết tối ưu trải nghiệm người dùng giúp tăng tỷ lệ chuyển đổi cho dự án web.
   *(Các thẻ cards áp dụng hiệu ứng `:hover` nổi khối và đổ bóng sâu).*

4. **Speakers & Agenda Section (Diễn giả & Lịch trình):**
   - Giới thiệu ngắn gọn về chuyên gia hướng dẫn (Ảnh đại diện, Họ tên, Chức vụ).
   - Lịch trình tóm tắt các phiên chia sẻ từ cơ bản đến nâng cao.

5. **Registration Form Section (Đăng ký tham gia):**
   - Tiêu đề: *Giữ chỗ sự kiện hoàn toàn miễn phí ngay hôm nay.*
   - Form gồm các trường: Họ và tên, Email, Số điện thoại, Vai trò hiện tại.
   - Nút Submit hoàn tất. *(Ô input có hiệu ứng `:focus` rõ ràng, bắt mắt).*

6. **Footer:**
   - Thông tin bản quyền, mạng xã hội và liên hệ ban tổ chức.

# Đầu ra mong đợi
- Mã nguồn **HTML5** chuẩn semantic, rõ ràng, có gắn link CDN của Animate.css và liên kết file CSS ngoài (`style.css`).
- Mã nguồn **CSS** đầy đủ, viết theo dạng external, bao gồm toàn bộ kiểu dáng giao diện, layout, hiệu ứng `:hover`, `:focus` và các tùy chỉnh tinh tế khác.

**Bản nền:** `index.html` và `style.css` ban đầu (đã có header, hero, benefits, speakers, agenda, form, footer, tone neon tối, AOS và Animate.css). Các lần tinh chỉnh bên dưới đều chỉnh sửa trực tiếp trên hai file này, không viết lại từ đầu.

## 2. Quá trình tinh chỉnh & Giải quyết sự cố (Iteration)

### Lần 1: Hiệu ứng lật mặt 3D cho thẻ Diễn giả
- **Prompt đã dùng:** Cấu trúc lại thẻ diễn giả thành dạng thẻ lật: `.speaker-card` (có `perspective: 1000px`) chứa `.speaker-card-inner` với hai mặt `.speaker-card-front` (ảnh, tên, chức vụ) và `.speaker-card-back` (tiểu sử). Khi hover thì `rotateY(180deg)` với `transform-style: preserve-3d` và `backface-visibility: hidden`.
- **Kết quả AI tạo ra:** Cấu trúc HTML mới cho 3 diễn giả, mặt sau có tiểu sử và thẻ kỹ năng; CSS lật 0,8 giây, thêm `tabindex="0"` và `:focus-within` để lật được bằng bàn phím và chạm trên điện thoại.
- **Nhận xét & Tinh chỉnh của SV:** Phải bỏ `overflow: hidden` ở khung ngoài và chuyển nền, viền sang từng mặt thẻ, vì `overflow: hidden` làm hỏng hiệu ứng 3D. Phần tiểu sử là nội dung mẫu do AI viết, cần thay bằng thông tin thật.

### Lần 2: Thẻ Lợi ích phát sáng khi hover
- **Prompt đã dùng:** Giữ nguyên nội dung 3 card (Tư duy thiết kế đỉnh cao, Thực hành thực tế 100%, Bí quyết độc quyền); áp dụng `:hover` nổi khối cực mạnh và phát sáng viền.
- **Kết quả AI tạo ra:** Card nhấc lên 18px và phóng 1,04 lần, viền gradient phát sáng bằng `::before` có `mask`, vầng sáng toả từ đỉnh thẻ, mỗi card một màu (cyan, tím, magenta), icon xoay nhẹ.
- **Nhận xét & Tinh chỉnh của SV:** Phát hiện AOS đặt `transform` lên phần tử và có thể chặn hiệu ứng hover, nên AI viết selector với độ ưu tiên cao hơn để hiệu ứng nâng thẻ vẫn chạy.

### Lần 3: Hiệu ứng gõ chữ (typing) bằng Pure CSS
- **Prompt đã dùng:** Dòng mô tả ở Hero phải tự gõ chữ bằng `@keyframes`, `steps()`, `overflow: hidden`, `white-space: nowrap` và con trỏ nhấp nháy bằng `border-right`. Tuyệt đối không dùng JavaScript.
- **Kết quả AI tạo ra:** Câu được tách thành 3 dòng, mỗi dòng gõ lần lượt, con trỏ chỉ hiện ở dòng đang gõ, dòng cuối nhấp nháy sau khi xong.
- **Nhận xét & Tinh chỉnh của SV:** Font Inter có độ rộng ký tự không đều nên `steps()` làm con trỏ bị lệch; AI chuyển dòng này sang font monospace (JetBrains Mono) để 1 bước bằng đúng 1 ký tự. Đã thêm `prefers-reduced-motion` để hiện chữ ngay cho người dùng giảm chuyển động.

### Lần 4: Cho hiệu ứng gõ chạy liên tục
- **Prompt đã dùng:** "Cần hiệu ứng typing lặp lại, liên tục".
- **Kết quả AI tạo ra:** Chu kỳ 10 giây lặp vô hạn: gõ 3 dòng, giữ chữ và nhấp nháy con trỏ, xóa lần lượt từ dòng 3 lên dòng 1, rồi gõ lại.
- **Nhận xét & Tinh chỉnh của SV:** Yêu cầu hơi mơ hồ nên AI đã hiểu theo hướng "lặp vô hạn". Cần nêu rõ hơn nếu muốn kiểu khác. Con trỏ được sửa để nhấp nháy dứt khoát (bật/tắt hẳn) thay vì mờ dần.

### Lần 5: Nút CTA chính nhịp đập và hover siêu mạnh
- **Prompt đã dùng:** Nút "Đăng Ký Giữ Chỗ Ngay" có hiệu ứng nhịp đập thu hút kết hợp hover siêu mạnh.
- **Kết quả AI tạo ra:** Nút đập hai nhịp như nhịp tim, hai vòng sóng cyan và magenta lan ra quanh nút; khi hover nút nổi lên, phóng 1,1 lần, gradient chảy kèm vệt sáng quét và vầng sáng nhiều lớp.
- **Nhận xét & Tinh chỉnh của SV:** Nút đã dùng `animate__fadeInUp` nên một animation thêm vào sẽ ghi đè nó. AI xử lý bằng cách gọi lại `fadeInUp` trong thuộc tính `animation` và viết nhịp đập bằng thuộc tính `scale` riêng, để không xung đột với `transform` của hover.

### Lần 6: Đồng hồ đếm ngược tĩnh và nâng cấp form đăng ký
- **Prompt đã dùng:** Thêm khối `.countdown-container` gồm Ngày, Giờ, Phút, Giây với giá trị gán sẵn, kiểu neon Cyberpunk, hover phóng to; đồng thời nâng cấp khung đăng ký, nút Submit và ô `input` khi `:focus`.
- **Kết quả AI tạo ra:** Bốn ô vuông nền tối viền neon (`03 : 12 : 45 : 30`) đặt trong cột bên trái phần đăng ký; form có viền sáng nhiều lớp khi hover, input có neon glow khi focus, nút Submit có hiệu ứng riêng.
- **Nhận xét & Tinh chỉnh của SV:** Sửa trực tiếp vào file có sẵn, không viết lại. Có thể đổi số giả định ngay trong HTML.

### Lần 7: Đồng hồ đếm ngược chạy bằng CSS Animation
- **Prompt đã dùng:** Dùng `@keyframes` để tạo chuyển động, thay đổi số, nhấp nháy hoặc chạy số giả lập hoàn toàn bằng Pure CSS cho cảm giác khẩn trương.
- **Kết quả AI tạo ra:** Số được đếm bằng thuộc tính `--count` khai báo qua `@property` kết hợp `counter()`; giây đếm lùi mỗi giây, phút/giờ/ngày giảm theo nhịp thật. Chữ số ô Giây "rơi" theo từng giây, 10 giây cuối mỗi phút viền hồng nhấp nháy, các ô khác thỉnh thoảng chớp như đèn neon.
- **Nhận xét & Tinh chỉnh của SV:** Cách này cần trình duyệt hỗ trợ `@property`. Người dùng bật giảm chuyển động sẽ thấy số tĩnh.

### Lần 8: Nền lưới Cyberpunk và vầng sáng neon
- **Prompt đã dùng:** Nền tối `#050814` hoặc `#0b0f19`, phủ lưới `linear-gradient` bằng đường kẻ cyan/tím mờ, `background-size` khoảng `40px 40px`; thêm 1 đến 2 vầng sáng `blur(80px)`, `opacity: 0.3`; không ảnh hưởng hover, thẻ lật 3D và form.
- **Kết quả AI tạo ra:** Lưới 40px (ngang cyan, dọc tím) trên `body::before`, mờ dần ra mép; hai vầng sáng `.orb-cyan` và `.orb-violet` trôi rất chậm, đều có `pointer-events: none`.
- **Nhận xét & Tinh chỉnh của SV:** Vầng sáng đặt trước `.page-shell` để nằm sau nội dung và không bị `overflow: hidden` cắt.

### Lần 9: Kiểm tra tích hợp Animate.css và AOS
- **Prompt đã dùng:** Kiểm tra tích hợp Animate.css và AOS đã đúng cách chưa.
- **Kết quả AI tạo ra:** Kết luận cả hai đã tích hợp đúng (link CDN, tiền tố class `animate__`, `AOS.init()`), kèm 4 điểm nên cải thiện.
- **Nhận xét & Tinh chỉnh của SV:** Phát hiện `data-aos-delay` làm hover của thẻ thứ 2 và 3 bị trễ, `data-aos` bị lồng nhau ở section Lợi ích, và AOS chưa tôn trọng `prefers-reduced-motion`. **Các điểm này đã được ghi nhận nhưng chưa sửa.**

### Lần 10: Kiểm tra CSS Variables, Flexbox/Grid, UI/UX
- **Prompt đã dùng:** Kiểm tra đã đủ yêu cầu về CSS Variables cho màu/font, layout Flexbox/Grid, UI/UX thẩm mỹ và hoàn thiện.
- **Kết quả AI tạo ra:** Layout đạt (16 chỗ dùng Flexbox, 11 chỗ dùng Grid, 3 mốc responsive); CSS Variables mới đạt một phần.
- **Nhận xét & Tinh chỉnh của SV:** Còn thiếu biến font, một số biến màu khai báo nhưng chưa dùng, và vài màu viết cứng. Form chưa có `required`, `autocomplete` hay thông báo lỗi; link mạng xã hội còn là `#`. **Chưa sửa.**

### Lần 11: Kiểm tra và sửa cấu trúc HTML semantic
- **Prompt đã dùng:** Kiểm tra cấu trúc web hợp lệ, dùng đúng thẻ ngữ nghĩa, không lạm dụng `<div>`; sau đó "áp dụng" các đề xuất.
- **Kết quả AI tạo ra:** Menu đổi thành `<ul>`; lịch trình thành `<ol>` với `<time>`; thông tin liên hệ vào `<address>`; mạng xã hội thành `<ul>`; tên diễn giả ở mặt sau thẻ lật đổi từ `<h3>` sang `<p>`; khối minh họa Hero đặt `aria-hidden`; 3 tiêu đề section đổi từ `<div>` sang `<header>`. Số `<div>` giảm từ 61 xuống 50, không có lỗi đóng/mở thẻ.
- **Nhận xét & Tinh chỉnh của SV:** CSS được chỉnh kèm (`list-style: none`, `font-style: normal`, selector `.speaker-name`) để giao diện giữ nguyên.

Lần 12: Refactoring và UI/UX Finalization
Prompt đã dùng: Tiến hành Refactoring và UI/UX Finalization (tinh chỉnh và hoàn thiện toàn diện) cho mã nguồn HTML và CSS; đảm bảo mã sạch, tối ưu hiệu năng, đồng bộ toàn bộ hiệu ứng và phong cách Cyberpunk/Tech hiện đại.
Kết quả AI tạo ra:
CSS Variables: thêm token màu dạng --cyan-rgb, --magenta-rgb... để toàn bộ rgba() dùng rgba(var(--cyan-rgb), 0.4); thêm biến font (--font-body, --font-mono), biến nền và --header-h; xóa các biến không dùng.
Dọn mã: gộp 5 khối prefers-reduced-motion thành 1; thay transition: all bằng danh sách thuộc tính cụ thể; bỏ rule hover thừa; chuyển style inline của đồng hồ và hiệu ứng gõ chữ vào CSS.
Hiệu năng: gộp 2 link Google Fonts thành 1, thêm preconnect, ảnh có width/height/loading="lazy", script AOS dùng defer, bỏ background-attachment: fixed.
Form: thêm required, autocomplete, inputmode, pattern cho số điện thoại và thông báo lỗi bằng CSS thuần (:user-invalid).
Trải nghiệm và truy cập: scroll-padding-top cho header dính, skip link, outline focus rõ, văn bản ẩn .sr-only cho hiệu ứng gõ chữ, thẻ theme-color, Open Graph và favicon.
AOS: chỉ giữ data-aos ở phần tử con, AOS.init({ once: true, duration: 700 }) tự tắt khi bật giảm chuyển động, sửa hover bị trễ và hover dòng lịch trình bị chặn, thêm <noscript>.
Nhận xét & Tinh chỉnh của SV: Kiểm tra bằng script: HTML không lỗi thẻ, ID không trùng, mọi anchor đều có đích, CSS cân ngoặc, không còn biến chưa khai báo hay biến thừa. Giao diện và các hiệu ứng cũ được giữ nguyên. Cần mở trang trên trình duyệt để xem lại thực tế, và thay link mạng xã hội bằng link thật.

## 3. Đánh giá cá nhân về quá trình Vibe Coding
- AI đã giúp bạn tiết kiệm thời gian ở phần nào nhất?
  - Các hiệu ứng CSS phức tạp: thẻ lật 3D, viền phát sáng, đồng hồ tự đếm bằng `@property`, nền lưới và vầng sáng. Ngoài ra AI giúp rà soát cả file để chỉ ra chỗ chưa đạt (semantic, biến CSS, tích hợp thư viện).
- Bài học rút ra khi đặt câu hỏi (Prompt) cho AI trong thiết kế web?
  - Nên yêu cầu "chỉnh sửa trực tiếp, không viết lại từ đầu" và nêu rõ ràng buộc kỹ thuật (Pure CSS, không JS), vì mỗi hiệu ứng mới dễ xung đột với cái cũ (AOS với hover, Animate.css với animation riêng). Yêu cầu mơ hồ như "gõ liên tục" sẽ bị AI diễn giải theo ý riêng nên cần mô tả cụ thể. Nên yêu cầu AI kiểm tra lại sau mỗi lần sửa và tự mở trang trên trình duyệt để thử, vì các lần kiểm tra ở trên đọc mã nguồn chứ chưa chạy giao diện thực tế.
- Những điểm còn tồn đọng?
  - Yêu cầu ban đầu cấm JavaScript, nhưng trang vẫn dùng thư viện AOS (`AOS.init()`), nên cần cân nhắc bỏ AOS hoặc thay bằng hiệu ứng CSS thuần để đúng ràng buộc. Ngoài ra còn các việc: sửa độ trễ hover do `data-aos-delay`, gom font và màu cứng về CSS Variables, thêm `required`/`autocomplete` cho form và gắn link thật cho mạng xã hội.