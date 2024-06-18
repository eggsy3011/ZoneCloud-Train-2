
# cp command
# cp file :
```
cp file.txt file_backup.txt 
```
![image](https://github.com/eggsy3011/ZoneCloud-Train-2/assets/108015833/dc8c3fe4-94b2-441d-a7d6-ee3e51c2a5f0)


# cp folder
```
cp -r  /123  /abctest
```
![image](https://github.com/eggsy3011/ZoneCloud-Train-2/assets/108015833/b0ff1e6b-560b-4bea-8a1d-5b3712ee88d8)


# mv command

mv file

![image](https://github.com/eggsy3011/ZoneCloud-Train-2/assets/108015833/6ef8da01-aebe-4e2f-8d00-4c994d5372d5)


folder

![image](https://github.com/eggsy3011/ZoneCloud-Train-2/assets/108015833/6b4feeec-cd5b-48a7-afb7-68d4f0078b38)



# cut command: Lệnh cut trong các hệ điều hành giống Unix được sử dụng để trích xuất các phần cụ thể của mỗi dòng từ đầu vào.

# Cut kí tự thứ <n> trong string
```
cut -c <n> tên_tệp 
```
ví dụ: Trích xuất ký tự từ vị trí thứ <n> trở đi (VD: từ vị trí thứ 10 đến cuối mỗi dòng)

![image](https://github.com/eggsy3011/ZoneCloud-Train-2/assets/108015833/9eaa36ab-770e-434c-b3f5-f61952467640)



# Cut từ kí tự thứ <n> trở về sau
```
cut -c <n>- tên_tệp
```
ví dụ:
Để trích xuất từ ký tự thứ 7 trở về sau của mỗi dòng trong tệp này: 

![image](https://github.com/eggsy3011/ZoneCloud-Train-2/assets/108015833/097d3ac6-7ed3-4d8c-8eb8-e93e59979208)

ví dụ: 

Để trích xuất từ đầu dòng đến ký tự thứ 5 của mỗi dòng trong tệp này

# Cut từ kí tự thứ <n> trở về trước


![image](https://github.com/eggsy3011/ZoneCloud-Train-2/assets/108015833/fc367190-4e79-4b47-b550-606d19c19be2)





# dig command:

Lệnh dig (Domain Information Groper) là một công cụ dòng lệnh được sử dụng để truy vấn thông tin DNS.

Dùng Dig command để kiểm tra resolv record A.

dig  dig google.com A: Bản ghi A ánh xạ tên miền tới địa chỉ IPv4. dig ex.com A

![image-10](https://github.com/eggsy3011/ZoneCloud-Train-2/assets/108015833/a603312d-468c-4485-b5fc-88e4ce0bf3d9)

![image-11](https://github.com/eggsy3011/ZoneCloud-Train-2/assets/108015833/5eb16f0f-6f51-4279-9c96-61cd4b8e9944)

# MX: Bản ghi MX chỉ định máy chủ thư điện tử cho tên miền. dig ex.com MX

![image-12](https://github.com/eggsy3011/ZoneCloud-Train-2/assets/108015833/d7cc17e2-b4d2-4b6b-8582-d3274eca9706)



# NS: Bản ghi NS chỉ định máy chủ tên miền cho tên miền. dig ex.com NX

![image-13](https://github.com/eggsy3011/ZoneCloud-Train-2/assets/108015833/158467d4-1f32-4e58-94c9-38a5b9d96f50)


# Dùng Dig command để kiểm tra resolv record A, MX, NS với custom DNS
```
A :  dig @<dns-server> <domain> A
```
# dig @8.8.8.8 google.com A

![image-14](https://github.com/eggsy3011/ZoneCloud-Train-2/assets/108015833/a28ace27-e940-45b0-9ebe-d73db4e47285)


# MX: dig @8.8.8.8 google.com MX
![image-15](https://github.com/eggsy3011/ZoneCloud-Train-2/assets/108015833/b223349b-d379-4a8f-9a52-6950fbd4f102)


# NS: dig @8.8.8.8 google.com NS

![image-16](https://github.com/eggsy3011/ZoneCloud-Train-2/assets/108015833/4310e934-bc91-4d8d-be43-f3655a2daf87)


# tar/zip/unzip command

# nén file tar.gz 
```
tar -czvf ten_file.tar.gz ten_file
```
-c: Tạo tệp mới.

-z: Sử dụng gzip để nén.

-v: Hiển thị tiến trình trên màn hình.

-f: Xác định tên của tệp nén.

![image-17](https://github.com/eggsy3011/ZoneCloud-Train-2/assets/108015833/48469f26-9bda-4d1c-998e-a1f2ccd37219)


# Giải nén file tar.gz: 
```
tar -xzvf ten_file.tar.gz
```
-x: Trích xuất các tệp từ tệp nén.

-z: Sử dụng gzip để giải nén.

-v: Hiển thị tiến trình trên màn hình.

-f: Xác định tên của tệp nén.

![image-18](https://github.com/eggsy3011/ZoneCloud-Train-2/assets/108015833/15f3df53-6888-4de4-8c46-57f31474a98a)


 # Nén/Giải nén file .zip
```
 zip ten_file.zip ten_file
```
![image-19](https://github.com/eggsy3011/ZoneCloud-Train-2/assets/108015833/1d164cdf-901b-49ed-a0fc-ba6abaa509dd)

```
unzip ten_tep.zip
```
![image-20](https://github.com/eggsy3011/ZoneCloud-Train-2/assets/108015833/7c0d28f9-d8a5-4c21-b951-2f6d116bff04)

# mount/umount command

- Add thêm một ổ cứng sdb ~ 5gb 
- Kiểm tra được có bao nhiêu ổ cứng trên máy chủ: lsblk

![image-21](https://github.com/eggsy3011/ZoneCloud-Train-2/assets/108015833/d50839df-e265-47f7-a155-9ffee53e2316)


#  Mount ổ cứng vào /mnt/test 
```
mkdir -p /mnt/test
```
# Umount /mnt/test
```
umount /mnt/test
```
# Symbolic Links, Hard Links command

# Symbolic Links (Sym Links):

    Định nghĩa: Symbolic Links, còn được gọi là soft links, là các liên kết tệp hoặc thư mục mà chỉ chứa đường dẫn tuyệt đối hoặc tương đối đến tệp hoặc thư mục gốc. Nói cách khác, một symbolic link chỉ là một con trỏ đến tệp hoặc thư mục khác trên hệ thống tệp.

    Tính linh hoạt: Symbolic links có tính linh hoạt cao vì chúng có thể được tạo ra hoặc xóa bất kỳ lúc nào mà không ảnh hưởng đến tệp hoặc thư mục gốc.

Định nghĩ Hard Link:

# Định nghĩa: Hard Links là các liên kết tệp hoặc thư mục mà tham chiếu trực tiếp đến vùng dữ liệu của tệp hoặc thư mục gốc. Một hard link thực sự là một tên khác cho cùng một nội dung dữ liệu trên ổ đĩa.

Không thể tạo cho thư mục: Hard links không thể được tạo cho các thư mục. Chúng chỉ có thể được tạo cho các tệp.

# Ví dụ về Sym Link và Hard Link :

Ex: sym link : 
```
Symlink: Một "đường tắt" hoặc "shortcut" trỏ tới một tệp hoặc thư mục khác. Nó chứa thông tin về vị trí của tệp hoặc thư mục đích nhưng không chứa nội dung thực tế của tệp đó.

Không chia sẻ inode với tệp đích: Symlink có inode riêng của nó. Nó chỉ chứa đường dẫn tới tệp đích chứ không phải dữ liệu thực tế của tệp đó.

Có thể trỏ đến bất kỳ đâu: Symlink có thể trỏ tới tệp hoặc thư mục trên cùng hoặc khác hệ thống tệp.

Có thể liên kết thư mục: Bạn có thể tạo symlink cho cả tệp và thư mục.

Dễ bị đứt (dangling link): Nếu tệp hoặc thư mục đích bị xóa hoặc di chuyển, symlink sẽ trở thành "dangling link" (liên kết đứt gãy) và không còn hợp lệ.
```
# Ta tạo sym link có tên softlink.txt trỏ về file_name.txt, và softlink_folder.txt trỏ về folder_name.
```
ln -s file_name.txt softlink.txt
```
```
ln -s folder_name softlink_folder.txt
```
```
ls -i 
```
```
ll - i
``` 
![image](https://github.com/eggsy3011/ZoneCloud-Train-2/assets/108015833/94393304-885b-436d-90dc-c9bf6eb54896)


![image](https://github.com/eggsy3011/ZoneCloud-Train-2/assets/108015833/99c7c41a-cc54-4217-b3bb-6bd1c627fd63)



# Hard Link: Tạo Hardlinks có tên hardlink.txt trỏ về file_name.txt
```
ln file_name.txt hardlink.txt
```
```
ll -i
```
![image](https://github.com/eggsy3011/ZoneCloud-Train-2/assets/108015833/c5e88829-00ef-4330-82d8-d75db2c3e89a)



nếu chúng ta thêm dữ liệu vào file hardlink.txt cũng đồng nghĩa dữ liệu đó được thêm vào file_name.txt

![image](https://github.com/eggsy3011/ZoneCloud-Train-2/assets/108015833/e9cc0ef6-ffcc-4ead-bbf5-610485b6c7f7)



như chúng ta thấy nội dung 2 file y nhau nếu ta xóa 1 file cũng k ảnh hưởng gì file còn lại.

![image](https://github.com/eggsy3011/ZoneCloud-Train-2/assets/108015833/527a9a3c-558b-4e26-9722-f5d8acf4da29)


NOTE : 

Thêm dữ liệu: Thêm dữ liệu vào bất kỳ hard link nào sẽ ảnh hưởng đến tất cả các hard link khác, vì tất cả đều trỏ tới cùng một inode và do đó cùng một dữ liệu.

Xóa tệp: Xóa một hard link không ảnh hưởng đến dữ liệu nếu còn ít nhất một hard link khác trỏ tới cùng inode. Dữ liệu chỉ bị xóa khỏi hệ thống tệp khi tất cả các hard link tới inode đó bị xóa.


# Ls command


Liệt kê danh sách file/thư mục
```
ls
```
```
ls -a 
```
![image-29](https://github.com/eggsy3011/ZoneCloud-Train-2/assets/108015833/6be48214-d179-4e4b-bf7c-536488537faa)

```
ls /etc
```
![image-30](https://github.com/eggsy3011/ZoneCloud-Train-2/assets/108015833/e16797de-86da-4fa6-847c-f4638ca8fdcb)

```
ls -la
```
Show file ẩn


![image](https://github.com/eggsy3011/ZoneCloud-Train-2/assets/108015833/4cae58fe-dbd0-4700-bfdd-108ef135f6a3)




# Ps command : ps (hay Process Status) là một tiện ích của Unix/Linux dùng để xem thông tin của các tiến trình đang chạy trong hệ thống

show tiến trình 
```
ps -a 
```
```
ps -e 
```
![image-32](https://github.com/eggsy3011/ZoneCloud-Train-2/assets/108015833/629df75b-0349-4f60-b65c-203c3b7ff53c)


# Để xem mọi tiến trình của người dùng root
```
ps -U root -u root -N
```
![image-33](https://github.com/eggsy3011/ZoneCloud-Train-2/assets/108015833/97fdc048-7244-489f-8794-08914724f994)


# Để xem các tiến trình chạy bởi người dùng abc
```
ps -u abc
```
![image-34](https://github.com/eggsy3011/ZoneCloud-Train-2/assets/108015833/ceae5488-9def-4bb7-8cb2-c04d99c58673)


# Kill tiến trình
```
kill [Signal_or_Option] pid 
```
![image-35](https://github.com/eggsy3011/ZoneCloud-Train-2/assets/108015833/6ba4793c-15ac-4888-b03a-206bc2d89547)


# Top command : top là một công cụ trong Linux giúp bạn có thể theo dõi tình trạng hệ thống, các process đang chạy, CPU, Memory theo thời gian thực.

Kiểm tra tài nguyên cpu đang sử dụng của một vài process đang chạy.

![image-36](https://github.com/eggsy3011/ZoneCloud-Train-2/assets/108015833/a0a02df9-6d63-4f3f-803a-20f418bb9e24)


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

# Free command

![image](https://github.com/eggsy3011/ZoneCloud-Train-2/assets/108015833/bc9edf17-8fe2-4bf8-b0bc-5a7b11e750c5)



Giải thích ram used, free, shared, buff/cache, free

total: Hệ thống có 16,047,948 KB RAM.

used: Hiện tại đang có 6,016,360 KB RAM đang được sử dụng.

free: Có 7,185,896 KB RAM còn trống.

shared: Có 1,504,164 KB RAM đang được chia sẻ.

buff/cache: Có 4,681,884 KB RAM đang được sử dụng bởi bộ nhớ đệm và cache.

available: Khoảng 10,031,588 KB RAM có sẵn cho các ứng dụng mới.


# df command : Lệnh df trong Linux được sử dụng để hiển thị thông tin về dung lượng ổ đĩa của các phân vùng tệp hệ thống.

Xem dung lượng disk:
```
df - h 
```
![image-38](https://github.com/eggsy3011/ZoneCloud-Train-2/assets/108015833/2c3394d8-9246-48f1-9e46-a991bf4a392c)




# 1./ (Root)
Định nghĩa: Đây là phân vùng gốc của hệ thống. Tất cả các thư mục và tệp tin khác đều nằm dưới phân vùng này.
Ví dụ: Khi bạn cài đặt một hệ điều hành Linux, phân vùng / là nơi mà tất cả các tệp hệ thống và thư mục khác được cài đặt. Đây là nơi bắt đầu của cấu trúc thư mục.
# 2.. /boot
Định nghĩa: Phân vùng này chứa các tệp tin cần thiết để khởi động hệ điều hành, chẳng hạn như các kernel và các tệp khởi động.
Ví dụ: Khi máy tính của bạn khởi động, nó sẽ sử dụng các tệp tin trong phân vùng /boot để nạp hệ điều hành vào bộ nhớ.
# 3. /home
Định nghĩa: Đây là phân vùng chứa các thư mục cá nhân của người dùng. Mỗi người dùng trên hệ thống sẽ có một thư mục riêng trong /home.
Ví dụ: Nếu bạn có người dùng tên là alice, thì thư mục cá nhân của cô ấy sẽ là /home/alice, nơi lưu trữ tất cả các tệp tin và cài đặt cá nhân của cô ấy.
# 4. /swap
Định nghĩa: Phân vùng swap được sử dụng như bộ nhớ ảo. Khi RAM của bạn đầy, hệ thống sẽ sử dụng phân vùng swap để lưu trữ tạm thời các dữ liệu không cần thiết ngay lập tức.
Ví dụ: Nếu bạn đang chạy nhiều ứng dụng nặng và RAM của bạn bị đầy, hệ thống sẽ chuyển một số dữ liệu từ RAM sang phân vùng swap để giải phóng bộ nhớ.
# 5. ext4
Định nghĩa: Đây là một hệ thống tệp (filesystem) phổ biến trên Linux. Nó được thiết kế để quản lý và lưu trữ dữ liệu trên đĩa cứng.
Ví dụ: Khi bạn định dạng một ổ đĩa cứng hoặc phân vùng với ext4, hệ thống tệp này sẽ được sử dụng để tổ chức và quản lý dữ liệu trên phân vùng đó.
# 6. sfts (SFTP - Secure File Transfer Protocol)
Định nghĩa: Đây là một giao thức mạng an toàn để truyền tệp qua mạng. Nó sử dụng SSH để cung cấp một lớp bảo mật cho quá trình truyền tệp.
Ví dụ: Khi bạn muốn truyền tệp từ máy tính của mình lên một máy chủ từ xa một cách an toàn, bạn có thể sử dụng SFTP. Ví dụ, lệnh sftp user@remote-server sẽ mở kết nối SFTP đến máy chủ từ xa và bạn có thể truyền tệp qua kết nối này.

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
