
cp command

cp file :

cp file.txt file_backup.txt

![alt text][def]

cp folder

cp file.txt /2

![alt text][def2]

mv command

mv file


![alt text][def3] 


folder

![alt text][def4]

cut command: Lệnh cut trong các hệ điều hành giống Unix được sử dụng để trích xuất các phần cụ thể của mỗi dòng từ đầu vào.

cut kí tự thứ <n> trong string

cut -c <n> tên_tệp

ví dụ ta có tệp sau để cut 

![alt text][def5]

![alt text][def6]

cut từ kí tự thứ <n> trở về sau

cut -c <n>- tên_tệp

![alt text][def7]

cut từ kí tự thứ <n> trở về trước

![alt text](image-9.png)

dig command:

Lệnh dig (Domain Information Groper) là một công cụ dòng lệnh được sử dụng để truy vấn thông tin DNS.

Dùng Dig command để kiểm tra resolv record A.

dig  dig google.com A: Bản ghi A ánh xạ tên miền tới địa chỉ IPv4. dig ex.com A

![alt text][def9]


MX. Bản ghi MX chỉ định máy chủ thư điện tử cho tên miền. dig ex.com MX

![alt text][def10]

NS. Bản ghi NS chỉ định máy chủ tên miền cho tên miền. dig ex.com NX

![alt text][def11]

Dùng Dig command để kiểm tra resolv record A, MX, NS với custom DNS

A :  dig @<dns-server> <domain> A

dig @8.8.8.8 google.com A

![alt text][def12]

MX: dig @8.8.8.8 google.com MX

![alt text][def13]

NS: dig @8.8.8.8 google.com NS

![alt text][def14]

tar/zip/unzip command

nén file tar.gz 

tar -czvf ten_file.tar.gz ten_file

-c: Tạo tệp mới.
-z: Sử dụng gzip để nén.
-v: Hiển thị tiến trình trên màn hình.
-f: Xác định tên của tệp nén.

![alt text][def15]

Giải nén file tar.gz: 

tar -xzvf ten_file.tar.gz

-x: Trích xuất các tệp từ tệp nén.
-z: Sử dụng gzip để giải nén.
-v: Hiển thị tiến trình trên màn hình.
-f: Xác định tên của tệp nén.

![alt text][def16]

 Nén/Giải nén file .zip

 zip ten_file.zip ten_file

![alt text][def17]

unzip ten_tep.zip

![alt text][def18]


mount/umount command

- Add thêm một ổ cứng sdb ~ 5gb
- 

- Kiểm tra được có bao nhiêu ổ cứng trên máy chủ: lsblk

![alt text][def19]

- Mount ổ cứng vào /mnt/test 

mkdir -p /mnt/test
  
- Umount /mnt/test

umount /mnt/test

Symbolic Links, Hard Links command

Định nghĩ Sym Link: 
Symbolic Links (Sym Links):

    Định nghĩa: Symbolic Links, còn được gọi là soft links, là các liên kết tệp hoặc thư mục mà chỉ chứa đường dẫn tuyệt đối hoặc tương đối đến tệp hoặc thư mục gốc. Nói cách khác, một symbolic link chỉ là một con trỏ đến tệp hoặc thư mục khác trên hệ thống tệp.

    Tính linh hoạt: Symbolic links có tính linh hoạt cao vì chúng có thể được tạo ra hoặc xóa bất kỳ lúc nào mà không ảnh hưởng đến tệp hoặc thư mục gốc.

Định nghĩ Hard Link:

Định nghĩa: Hard Links là các liên kết tệp hoặc thư mục mà tham chiếu trực tiếp đến vùng dữ liệu của tệp hoặc thư mục gốc. Một hard link thực sự là một tên khác cho cùng một nội dung dữ liệu trên ổ đĩa.

Không thể tạo cho thư mục: Hard links không thể được tạo cho các thư mục. Chúng chỉ có thể được tạo cho các tệp.

Ví dụ về Sym Link và Hard Link :

Ex: sym link : 

Ta tạo sym link có tên softlink.txt trỏ về file_name.txt, và softlink_foldẻ.txt trỏ về foldẻ_name.

ln -s file_name.txt softlink.txt

ln -s folder_name softlink_folder.txt

ls -i 

ll - i 

![alt text][def20]

![alt text][def23]

Hard Link: Tạo Hardlinks có tên hardlink.txt trỏ về file_name.txt

ln file_name.txt hardlink.txt

ll -i

![alt text][def21]

nếu chúng ta thêm dữ liệu vào file hardlink.txt cũng đồng nghĩa dữ liệu đó được thêm vào file_name.txt

![alt text][def22]

![alt text][def24]

như chúng ta thấy nội dung 2 file y nhau nếu ta xóa 1 file cũng k ảnh hưởng gì file còn lại.

![alt text][def25]

ls command


Liệt kê danh sách file/thư mục

ls

ls -l 

![alt text][def26]

ls -a 

![alt text][def27]

ls /etc

![alt text](image-30.png)

ls -a | grep "^\\."

Show file ẩn

![alt text][def28] 

ps command : ps (hay Process Status) là một tiện ích của Unix/Linux dùng để xem thông tin của các tiến trình đang chạy trong hệ thống

show tiến trình 

ps -a 

ps -e 

![alt text][def29]

Để xem mọi tiến trình của người dùng root

ps -U root -u root -N

![alt text][def30]

Để xem các tiến trình chạy bởi người dùng abc

ps -u abc

![alt text][def31]

kill tiến trình

kill [Signal_or_Option] pid 

![alt text][def32]

top command : top là một công cụ trong Linux giúp bạn có thể theo dõi tình trạng hệ thống, các process đang chạy, CPU, Memory theo thời gian thực.

Kiểm tra tài nguyên cpu đang sử dụng của một vài process đang chạy.

![alt text][def33]

Giải thích về Load average, us, sy, ni, id, wa, hi, si, st, zombie process, sleeping process.


Load average: Đây là trung bình của tải hệ thống trong khoảng thời gian 1, 5 và 15 phút gần đây.

us (user): Thời gian CPU được sử dụng bởi các tiến trình người dùng.

sy (system): Thời gian CPU được sử dụng bởi hệ thống.

ni (nice): Thời gian CPU được sử dụng bởi các tiến trình ưu tiên (nice).

id (idle): Thời gian CPU không hoạt động.

wa (waiting): Thời gian CPU đang chờ I/O.

hi (hardware interrupt): Thời gian CPU xử lý các ngắt phần cứng.

si (software interrupt): Thời gian CPU xử lý các ngắt phần mềm.

st (stolen): Thời gian CPU bị ăn cắp bởi máy ảo (nếu có).

Zombie process: Tiến trình đã kết thúc nhưng vẫn còn trong bộ nhớ.

Sleeping process: Tiến trình đang chờ sự kiện nào đó để thực hiện tiếp


free command

![alt text][def34]

Giải thích ram used, free, shared, buff/cache, free

total: Hệ thống có 16,047,948 KB RAM.

used: Hiện tại đang có 6,016,360 KB RAM đang được sử dụng.

free: Có 7,185,896 KB RAM còn trống.

shared: Có 1,504,164 KB RAM đang được chia sẻ.

buff/cache: Có 4,681,884 KB RAM đang được sử dụng bởi bộ nhớ đệm và cache.

available: Khoảng 10,031,588 KB RAM có sẵn cho các ứng dụng mới.


df command : Lệnh df trong Linux được sử dụng để hiển thị thông tin về dung lượng ổ đĩa của các phân vùng tệp hệ thống.

Xem dung lượng disk:

df - h 

![alt text][def35]


Phân vùng / là gì 

Phân vùng / (root) là phân vùng gốc của hệ thống tệp trong Linux. Đây là nơi bắt đầu của cấu trúc thư mục trong hệ điều hành, và tất cả các tệp và thư mục khác đều nằm trong phân vùng này hoặc trong các phân vùng khác được gắn kết vào hệ thống tệp tại các điểm khác nhau.

Phân vùng tmpfs là gì

 là một loại hệ thống tệp đặc biệt sử dụng RAM làm phương tiện lưu trữ thay vì đĩa cứng. Điều này có nghĩa là dữ liệu trong tmpfs sẽ được lưu trữ tạm thời trong bộ nhớ RAM và sẽ bị mất khi hệ thống khởi động lại.

#

Tìm hiểu về LVM 

Bài tập: Tạo PV, VG, LV, Extend LVM. Note lại quá trình cũng như các command sử dụng vào file markdown và lưu tại: <name>/linux/linux-basic/lvm.md

LVM là gì ?

LVM (Logical Volume Manager) là một công cụ trong hệ điều hành Linux cho phép quản lý không gian lưu trữ trên các ổ đĩa mềm dẻo (logical volumes) thay vì sử dụng trực tiếp các phân vùng cứng. LVM cho phép linh hoạt trong việc phân chia, mở rộng và thu hẹp các không gian lưu trữ mà không làm ảnh hưởng đến dữ liệu đã tồn tại.

Physical Volume: 

Physical Volume là khối xây dựng cơ bản của LVM. PV có thể là toàn bộ một ổ đĩa cứng hoặc một phân vùng đĩa cứng. PV chứa các khối dữ liệu (block) mà LVM sử dụng để lưu trữ dữ liệu.

Volume Group:

Volume Group là một tập hợp các Physical Volume. VG cung cấp một không gian lưu trữ tổng hợp mà từ đó bạn có thể tạo các Logical Volume. VG có thể được mở rộng bằng cách thêm PV mới.

Logical Volume:

Logical Volume là các phân vùng ảo được tạo ra từ không gian của Volume Group. LV hoạt động tương tự như các phân vùng thông thường và có thể chứa hệ điều hành, ứng dụng, và dữ liệu người dùng. Bạn có thể dễ dàng mở rộng hoặc thu nhỏ LV mà không cần phân vùng lại ổ đĩa.



[def]: image-2.png
[def2]: image-3.png
[def3]: image-4.png
[def4]: image-5.png
[def5]: image-6.png
[def6]: image-7.png
[def7]: image-8.png
[def8]: image-10.png
[def9]: image-11.png
[def10]: image-12.png
[def11]: image-13.png
[def12]: image-14.png
[def13]: image-15.png
[def14]: image-16.png
[def15]: image-17.png
[def16]: image-18.png
[def17]: image-19.png
[def18]: image-20.png
[def19]: image-21.png
[def20]: image-22.png
[def21]: image-24.png
[def22]: image-25.png
[def23]: image-23.png
[def24]: image-26.png
[def25]: image-27.png
[def26]: image-28.png
[def27]: image-29.png
[def28]: image-31.png
[def29]: image-32.png
[def30]: image-33.png
[def31]: image-34.png
[def32]: image-35.png
[def33]: image-36.png
[def34]: image-37.png
[def35]: image-38.png