Vagrant 

1.Tại sao sử dụng Vagrant??
- Vagrant cung cấp dễ dàng để cấu hình, tái sản xuất , và môi trường làm việc di động được xây dựng trên công nghệ tiêu chuẩn công nghiệp và được kiểm soát bởi một công việc phù hợp nhất để giúp tối đa hóa năng suất và tính linh hoạt của bạn và nhóm của bạn
- Vagrant có thể cung cấp máy chạy trên nhiều nền tảng khác nhau như Virtualbox,Vmware,AWS, hoặc bất kì nhà cung câp nào khác.
- Sau khi đã có nền tảng triển khai, vagrant có thể sủ dụng các kịch bản shell,Chef,.. để có thể tự động cài tất cả các goistreen máy ảo vagrant vừa tao ra.

2.Cài đặt và sử dụng vagrant:

- Để có thể chạy vagrant bạn cần có :
 + Vagrant
 + Virtualbox(VMware) khuyên dùng Virtualbox.
 + Linux(Ubuntu desktop).
 
- Vagrant có thể cái đặt trên nhiều hệ điều hành
- Cài đặt vagrant vô cùng đơn giản.Đầu tiên bạn vào trang chủ vagrant để tải về.Link <a href="">Link</a>
- Cài đặt bằng lệnh trong console:
```
 apt-get install vagrant -y
```

- Cài đặt virtualbox(hoặc Vmware Workstation).Ở đây tôi dùng Virtualbox trên OS là Ubuntu desktop 14.04.1:
```
apt-get install virtualbox -y
apt-get install dkms -y
```

Như vậy quá trình cài đặt hoàn tất.Bây giờ sẽ là một số lệnh cơ bản để sử dụng vagrant.

3.Sử dụng vagrant để tạo máy nhanh chóng :

- Để tạo được máy ảo bằng vagrant bạn cần phải có một file .vbox (hoăc .vmdk).Bạn có thể tải file box này từ đây <a href="http://cloud-images.ubuntu.com/vagrant">Link</a>.
hoặc <a href="http://www.vagrantbox.es/">đây</a> hoặc <a href="http://files.vagrantup.com/precise32.box">đây</a>.
- Hoặc bạn có thể tạo ra file box theo cú pháp sau:
```
vagrant box add my-box /path/to/the/new.box
```
- Ví dụ :
```
vagrant box add udemo http://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-amd64-vagrant-disk1.box
```
- Bạn có thể tạo ra file box bằng cách sử dụng giao diện của virtualbox.
- Chạy lệnh để tạo ra file vagrantfile:
```
vagrant init udemo
```
- Sau khi chạy xong lệnh trên bạn sẽ thấy hệ thống xuất hiện file Vagrantfile.
- Trong  file Vagrantfile sẽ có một số thông số quan trọng như sau: vi Vagrantfile.

Chỉnh sửa như sau:

```
config.vm.box = "base" => config.vm.box = "udemo"
```

- Lưu file và bắt đầu tạo máy :
```
vagrant up udemo
```
- Sau khi máy tạo xong. bạn dùng lệnh:

```
vagrant ssh udemo
```
để có thế  truy cập máy bạn vừa tạo.

=======
Còn tiếp.










