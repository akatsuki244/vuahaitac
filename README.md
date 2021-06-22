# vuahaitac
Client Nguồn: https://drive.google.com/drive/folders/1VQ-W9_Vmd5JAvEt16TNLTd9ssAE0UcQG

Mình lấy toàn bộ từ nguồn của bác famypo về việt hóa và không thêm tính năng nào mới cả.

Bài viết này mình sẽ hướng dẫn các bác việt hóa, đổi IP để chơi game trên Hamachi hoặc LAN cũng như chia sẽ trang AdminCP mà mình viết riêng cho server này.

Link Youtube Của Bạn P Gaming làm lại theo các bước của mình: https://www.youtube.com/watch?v=Ej1ql4iviDU
Các bạn có thể dựa theo video thực tế này để cài theo.

Toàn bộ TOOL: https://drive.google.com/drive/folders/12PUWqiV0nI4RsTsIJxwNvqt6xI3OHmeb

totalcmd: tool dùng để so sánh 2 thư mục, cũng như so sanh sự khác nhau của 2 file. Các bạn có thể tìm phần mềm tương tự.
ffdec: tool dùng để đọc file SWF Free.
Directory Lister Enterprise: tool dùng để lấy đường dần các file trong thư mục. Mục đích để RIP toàn bộ web khác về tưng ứng những file nằm trong thư mục.
httrack: tool dùng để tải các link được lấy từ Directory Lister Enterprise các bạn vào thư mục tương ứng coi cách setup nhé. Mình có 1 file NOTE.txt ở đó để hướng dẫn.
WinSCP: tool dùng để chép file vào trong Server
putty: tool dùng để connect gõ lệnh.
SecureCRT: tool cũng dũng để connect gõ lệnh nhưng thêm một số nút nhanh để dễ dàng bấm khỏi mất công gõ.
Navicat: tool dùng để truy cập Database My SQL

Phần 1: Hướng dẫn việt hóa

Bạn nào chỉ cần chơi thì bỏ qua phần này và kéo xuống dưới để tải server về chơi cũng như cofig mạng LAN chơi với bạn bè.

Thư Mục RIP từ haitacviet: https://drive.google.com/drive/folders/1QfUcI8SX-vUFAyjqE8i4UepPEvEodDsN

1. file xmls.txt thì đổi tên file lại là xmls.zip và giải nén ra 1 thư mục file .xml và mở từng file ra việt hóa hoặc tải thư mục RIP từ haitacviet về và so sanh 2 bên copy qua cẩn thận là được.
2. Các file Main.swf. Các bạn dùng tool ffdec để mở file Main này, kéo xuống dưới cùng có 1 file tên là: CreateRoles_properties với lại Globalization_properties
Việt hóa xong 2 file trên là đã việt hóa 70% rồi đó.
3. Thư mục talk trong assets các bạn lấy y xì bên haitacviet về bỏ vào.. hơn 4k file trong đó.,
4. Cuối cùng là các file swf hiệu ứng. Nó nằm rãi rác trong thư mục assets, phần lớn nằm trong thư mục swfs với modileUI

Xong rồi và ra tận hưởng thành quả.

Phần 2: Hướng dẫn cài đặt và chạy Server
Link Server: https://drive.google.com/file/d/1LG2CATIDP2vjXNbtbkhu92VThlgwFNJ0/view

(Trong Server đã có sẵn Client rồi, Bác nào chỉ muốn lấy Client đã việt hóa thì vào Link này tải để khỏi phải tải file nặng kia về: https://drive.google.com/file/d/1LG2CATIDP2vjXNbtbkhu92VThlgwFNJ0/view )

Server có IP là 192.168.127.142

User/password: root/64403575

Server hiện tại đang dùng card mạng VMNet8 với đường mạng 192.168.127.0 Các bạn nhớ chỉnh lại card mạng các bạn đang dùng để về với đường mạng này nhé.

Sau khi chạy server xong mở tool SecureCRT.exe ra. Mình đã setup sẵn connect Server trong đó rồi cũng như đã quét virus cả rồi nha.

Các bạn chạy số 1.Start SQL Đợi nó chạy xong đến khi hiển thị "NOTICE: [pool pirate] 'user' directive" thì bấm tiếp 2.Start SV
(Hinh Ảnh Về Start Server: https://drive.google.com/drive/folders/1i_HsxVDDWztcWQZfeQEpzpZ4Dhz12pzG

Chạy xong server thì vào đường dẫn 192.168.127.142 để chơi game. Mình việt hóa luôn trang đăng nhập cho các bạn dễ dàng chơi game.

Trang AdminCP được để đường dẫn: 192.168.127.142/_admincp_v4
Hinh Ảnh Toàn Cảnh Về Trang AdminCP: https://drive.google.com/drive/folders/17QdHttYQrUPtrFziHfvj376msdyosOeT

Phần 3: Hướng dẫn đổi IP sang mạng LAN để chơi với bạn bè
Hình Ảnh Toàn Cảnh Về Đổi IP: https://drive.google.com/drive/folders/1K6rRY06LrqKjrnqcTRhOs_dSv-XH3WD2
Dùng Tool: WinSCP, putty Để thao tác nha

1. Chỉnh IP Server:
Chỉnh ở file: /etc/sysconfig/network-scripts/ifcfg-eth0

2 Chỉnh IP ở các File:
(old IP: 192.168.127.142)

/home/pirate/lcserver/conf/game20002.xml
/home/pirate/www/core/config.php
/home/pirate/www/app/dh/ajax.php
/home/pirate/www/app/Game/game.php
/home/pirate/www/T9NuoYa/T9NuoYa.html

Những file về API thêm đồng đội với vật phẩm của trang nguồn mình dùng mà không thấy hoạt động: cũng đổi IP trong này nữa luôn nhé.
/home/pirate/www/mail/addhero.php
/home/pirate/www/mail/item.php

Những API của Server: Đổi IP tương ứng luôn nhé.
/home/pirate/rpcfw/conf/WhiteList.cfg.php
/home/pirate/rpcfw/lib/api/hzw_addhero.php
/home/pirate/rpcfw/lib/api/hzw_mail.php
/home/pirate/rpcfw/lib/api/hzw_recharge.php
/home/pirate/rpcfw/optool/confServer.cfg.php

IP trong trang AdminCP:
/home/pirate/www/_admincp_v4/app/DbConfig.php

IP trong Database: Dùng navicat để mở database t9-rxhzw-web
Tới Table: server

Sau khi xong toàn bộ các bước trên các bạn reboot lại server rồi hãy làm các bước như Phần 2 nhé.

Phần 4: Hướng dẫn cài đặt Hamachi để chơi online với Bạn Bè

Hình Ảnh Tòa Cảnh Về Kết Nối Hamachi: https://drive.google.com/drive/folders/1fYc1MOYE5QMum0qoS9NJxJHCam-A0Deu
---------------------------------------------------
Cài Đặt Hamachi:
File cài đặt đã có sẵn ở trong thư mục root.
Dùng phần mềm SecureCRT hoặc Putty để thao tác

gõ lệnh:
rpm -ivh logmein-hamachi-2.1.0.101-1.x86_64.rpm
---------------------------------------------------
Kết Nối Hamachi:

0. Đổi card mạng máy ảo sang định dạng Bridge Và chỉnh lại IP ở phần trên đã nói sang đường mạng tương ứng.
VD nhà mình đường mạng router kết nối internet là 192.168.1.0 thì Chỉnh lại IP của Server là 192.168.1.142

Sau Đó đổi toàn bộ những file IP Server thành IP của Hamachi cung cấp (Xem lại Phần 3)

Kham khảo hình ảnh ở link:

1. Trước hết phải kiểm tra có connect internet chưa???
ping google.com => false thì gõ dhclient -v để nó lấy lại IP rồi gõ lại "ping google.com"

2. hamachi login
Nó OK thì gõ tiếp hamachi để kiểm tra trang thái

3. Sửa các file ở trên thành IP của Hamachi.

4. Để Chơi Được Hamachi thị tạo Room rồi gõ: hamachi join <roomID>

Xong tất cả thì chạy server tương tự như Phần 2

---------------------------------------------------
Kiểm Tra Server Đã Được Bật Để Lắng Nghe Đúng IP Chưa:
Dùng phần mềm SecureCRT hoặc Putty để thao tác

Lệnh: netstat -tulnp

Tìm đến dòng game20002 coi nó lắng nghe port 8002 ở IP nào. Đúng IP là vào game được.


Phần 5: Một Số Chỉnh Sửa Dành Cho Những Bạn Thích Tìm Tòi

Toàn bộ những cái mình biết đều nằm ở trang AdminCP rồi, Còn lại là mình không biết hay là tìm không thấy chổ để chinh.

Ngoài ra các bạn có thể chỉnh sửa thông tin vàng, chiến tích này nọ đâu game khi tạo account bằng cách:
File: /home/pirate/rpcfw/conf/User.cfg.php

Sửa các thông tin tương ứng thôi. MÌnh đã sửa sẵn trong file Server rồi. Bác nào muốn chỉnh lại thì chỉnh.

INIT_GOLD => Vàng
INIT_BELLY => Beri
INIT_VIP => Cấp VIP. Max 12
INIT_PRESTIGE => Chiến Tích

Quà Phản Hồi Max: Navicat - t_bbpay_gold - gold_num sửa thành 5000000 là được

Phần 6: Trang AdminCP Do Mình Viết Và Một Số Thông Tin
Hình Ảnh Toàn Cảnh Của Trang AdminCP: https://drive.google.com/drive/folders/17QdHttYQrUPtrFziHfvj376msdyosOeT

AdminCP mình đã add vào trong Server sẵn (Tải Server sau ngày 16/05/2020) và không cần tải ở đây

Bác nào đã tải server cũ thì chỉ cần tải Link AdminCP ở đây và dùng Tool WinSCP copy vào đúng chổ là được (/home/pirate/www/_admincp_v4/)
Link AdminCP V4: https://drive.google.com/file/d/1tg4SVNcnNIqIAyJsOreRfWxwvHmIfMwi/view

Đổi IP AdminCP tưng ứng với server: /home/pirate/www/_admincp_v4/app/DbConfig.php

Một Số tính năng của trang AdminCP này:
1. Thêm các thông tin cơ bản: Beri, Vàng, Chiến Tích, Danh Vọng, Kinh Nghiệm Bảo Thạch, VIP.
2. Thêm số Ảnh Hồn: Xanh, Tím, Lục.
3. Các loại đá, điểm: Điểm Nguyên Tố, Đá Khắc Ấn, Đá Hải Hồn, Đá Nguyên Tố, Đá Năng Lượng, Nhận Tố Ác Quỹ, Kinh Nghiệm Trái Ác Quỹ, ....
4. Reset một số thông tin sau khi đã dùng hết lượt trong ngày: Lượt Chế Tạo, Lượt Tầm Bảo, Lượt Lấy Haki....
5. Tâng 1 Cấp Tướng Chính để hoàn thành nhiệm vụ không phải ngồi farm kinh nghiệm ở những LV Cao.
6. Tâng Cấp đồng đội bằng với cấp tướng chính đồng thời chuyển sinh MAX tương ứng với cấp.
7. Thêm đồng đội vào tài khoản (Lưu Ý: Thoát game trước khi thêm!!!) -> Đồng đội sau khi thêm thành công sẽ được để vào trong tửu quán. Trang thêm đồng đội cũng liệt kê ra danh sách đồng đội để thêm để dễ dàng tìm ID.
8. Thêm Vật Phẩm. Trang đã chia các loại vật phẩm như trái ác quỹ, pet, ... ra từng tab để dễ dàng tìm ID. Không cần thoát game khi thêm vật phẩm.
9. Xem thông tin tài khoản: Sẽ liệt kê ra trong tài khoản có nhưng thông tin cơ bản nào. Bấm vào là biết à :v
10. Dành cho các Admin thực thụ: Gửi Toàn Server. Sẽ gửi vàng cho toàn server đại loại đèn bù các thứ á  Cũng như Reset tầm bảo, chế đồ các thứ đồng loạt cho toàn server luôn. (Tính năng cần Tài Khoản Admin, Các xem tài khoản ADMIN thì kéo xuống dưới)
11. Tùy chỉnh database: Tại đây có thể xóa toàn bộ account để cho những anh em nào không thích những account cũ còn tồn tại trong đây thì reset đi. Lúc này chỉ có những account của bạn, bạn bè của bạn tạo ra và đấu với nhau.
12. Kiểm tra máy chủ: Sẽ liệt kê ra nhưng file đang chạy của server. Bất kì file nào tắt đều làm cho Server lỗi hoặc không chạy được. Nhớ kiểm tra ở đây khi anh em thấy server lỗi.
13. Tool việt hóa. Tool này có hướng dẫn ở từng trang rồi, các bạn xem ở từng trang để biết cách việt hóa cũng như đã có sẵn những file mẫu. Lưu Ý chỉ dùng trên MAC, Win thôi.
Lỗi thường gặp khi dùng tool việt hóa (https://drive.google.com/file/d/11gpZu8_2ynJhnKDqIRJzqwxIm_KBcr_M/view)

Tài khoản ADMIN: admin/123456 (Tài khoản admin được thiết lập ở file: /home/pirate/www/_admincp_v4/function/AccountAdmin.php)
Bạn nào muốn đổi thì đều đổi được cả.

Cách phân biệt tính năng nào là của admin:
+ Màu đen: Không cần tài khoản admin.
+ Màu Xanh Dương: Cần tài khoản admin.
+ Màu xám trắng: Tính năng bị khóa.

Bạn cũng không cần nhập tài khoản admin vội do cái nút nào cần sẽ thông báo là nút đó cần tài khoản admin. Lúc này bận nhập cũng không muộn.

Tùy Chỉnh Để 1 số khóa một số tính năng hay chuyển tính năng đó về dạng cần tài khoản Admin:
Tất tần tật đều nằm ở file config.json: /home/pirate/www/_admincp_v4/config/config.json
Giải nghĩa một số trường:
enable -> Có cho phép tính năng đó được mở hay không?? Nếu = false thì tính năng bị sẽ bị vô hiệu hóa, bấm vào sẽ hiện thông báo tính năng đã bị vô hiệu hóa.
isAdmin -> Có cần tài khoản admin hay không. Nếu = true thì sẽ cần tài khoản admin.
value -> Giá trị cho từng nút. Đại loại mình đang mặc định bấm vào Thêm Beri sẽ được +1000000000 Beri. Nếu bạn muốn ít hơn hay nhiều hơn thì chỉnh ở đây. Lưu Ý đừng chỉnh quá cao. Lỗi account ráng chịu

Ngoài ra các bạn có thể tùy chỉnh chữ ở bất kì nơi đâu thành 1 chữ khác.
Tất tần tật đều nằm ở file: /home/pirate/www/_admincp_v4/config/language-vi/language.json
Mình làm ra file này để đưa tất cả chữ tiếng việt về 1 file đặng ai cần đổi trang admincp sang ngôn ngữ khác thì chỉ cần dịch file này là xong.


Phần 7: Cách Kết Nối Database Bằng Navicat Của Mình
Hình Ảnh Mô Tả Thao Tác: https://drive.google.com/drive/folders/1NUpVvPW4fGfc3KWodHHsY_6UvbFuazYh

1. Tạo kết nối MY SQL
2. Tạo tên kết nối. Đặt tên gì cũng được. Như hình là mình đặt VHT 142.
3. Tạo kết nối SSH với các thông tin:
Host: 192.168.127.142
Port: 22
User Name: root
Password: 64403575


Một Số Câu Hỏi Để Hoàn Thiện Trang AdminCP và Server

1. [Đã Fix] Mình chưa tìm được cách send Item vào trong thư. Bác nào biết mong chỉ giáo.
2. [Đã Fix] MÌnh đang làm Tool lấy thông tin các text đã việt hóa sang file xmls trung. Tool hoạt động rất tốt cho đến cái file itemconfig.xml. Bác nào làm được file này thì chỉ giáo với nhé, Mình dùng PHP để write vào file, NÓ Write được hết trừ kí hiệu xuống dòng và một ký hiệu khác.:
&#xD; &#xA;
3. Các sự kiện trong server có một vài sự kiện không biết làm sao để mở hoạt động nó. Đại loại sự kiện Cây Ác Ma.

Đấy là các câu hỏi mình muốn hỏi các bác. Bác nào biết thì chỉ giúp với ạ.

Mình xin cảm ơn
