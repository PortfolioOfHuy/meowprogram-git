---
title: GIT
layout: quote
---

# GIT

<Toc/>

---

# GIT Ignore

<v-clicks>

- File dùng để chỉ định những file hoặc thư mục mà Git sẽ bỏ qua, không theo dõi sự thay đổi.
- Các trường hợp cần sử dụng .gitignore:
  - File tạm thời
  - Dữ liệu mật
  - File cấu hình riêng của từng môi trường
- Lưu ý: Tên file là .gitignore (bao gồm cả dấu `.`)
- Các bước tạo file `.gitignore`:
  1. Tạo file `.gitignore`
  2. Thêm các tệp và thư mục bỏ qua vào file
  3. Commit file `.gitignore` này
  4. Kiểm tra lại file `.gitignore` này đã hoạt động chưa

</v-clicks>

---

# Sử dụng .gitignore để loại bỏ các file .txt

```html
*.txt # ignore tất cả file có đuôi txt abc.log # ignore file có tên abc.log bin/
# ignore thư mục bin obj/ # ignore thư mục obj
```

---

# GIT Branch

<v-clicks>

- là bản sao của toàn bộ dự án, cho phép phát triển và thử nghiệm tính năng mới mà không ảnh hưởng tới nhánh chính.
- Mỗi nhánh độc lập với nhau (không ảnh hưởng tới các nhánh khác), cho phép các developer làm việc đồng thời trên cùng một dự án
- Nhánh giúp quản lý và phân tách các tính năng của mỗi developer.
- Sau khi hoàn thành, các thay đổi từ các nhánh con có thể gộp vào nhánh chính.

</v-clicks>

---

# Tại sao brach (nhánh) quan trọng?

<v-clicks>

- Cho phép các developer làm việc 1 cách độc lập với các tính năng khác nhau mà không ảnh hưởng tới nhau.
- Giúp quản lý dự án và sửa lỗi dễ dàng hơn.

</v-clicks>

---

# Liệt kê

<v-clicks>

- `Default Branch (nhánh chính)`: khi tạo repository mới thì đây sẽ là branch mặc định tùy vào mình tạo có thể là master hoặc main
  <br>
  `Lưu ý:` nhánh này cần phải luôn duy trì trạng thái ổn định nhất của dự án.
- Để xem danh sách các nhánh có trong repository:

```html
PS A:\kich ban\git> git branch * master # * được xem là định vị bạn đang ở nhánh
nào
```

</v-clicks>

---

# Các lệnh cơ bản làm việc với nhánh

|                           |                                        |
| ------------------------- | -------------------------------------- |
| git brach                 | liệt kê tất cả branch trong repository |
| git branch ten_nhanh      | tạo mới một nhánh                      |
| git checkout ten_nhanh    | chuyển qua nhánh với ten_nhanh         |
| git branch -d ten_nhanh   | Xóa nhánh                              |
| git checkout -b ten_nhanh | Tạo và chuyển tới nhánh có ten_nhanh   |

---

# Ví dụ

<v-clicks>

1. Tạo nhánh mới có tên là new1

```html
git branch new1
```

2. Kiểm tra danh sách các nhánh

```html
git branch
```

3. Kết quả:

```html
PS A:\kich ban\git> git branch new1
```

```html
PS A:\kich ban\git> git branch * master new1
```

</v-clicks>

---

# Chuyển đổi Branch

<v-clicks>

1. Chuyển sang nhánh new1 bằng lệnh:

```html
git checkout new1
```

2. Kết quả:

```html
PS A:\kich ban\git> git checkout new1 Switched to branch 'new1'
```

```html
PS A:\kich ban\git> git branch master * new1
```

3. Hãy kiểm tra lại bằng lệnh:

```html
git branch
```

</v-clicks>

---

# Thực hành

1. Tạo file mới
2. Tạo repository
3. Tạo file gitignore
4. Tạo các file có các đuôi: txt, log.
5. Hãy commit file có tên là abc.log và git không thể theo dõi các file có đuổi txt

---

# Một vài lệnh khác:

<v-clicks>

- Tạo nhánh và chuyển sang nhánh đó ngay lập tức

```html
git checkout -b ten_nhanh
```

- Tạo nhánh từ commit hash cụ thể

```html
git checkout -b ten_nhanh a1b2c3d4
```

- Xóa nhánh đã tồn tại

```html
git branch -d ten_nhanh
```

- Xóa 1 nhánh có commit chưa gộp code vào nhánh chính

```html
git branch -D ten_nhanh
```

</v-clicks>

---

# Giới thiệu git graph trên vs code

---

# Quy tắc đặt tên nhánh

- Quy tắc đặt tên nhánh trên Git giúp duy trì cấu trúc và dễ hiểu cho dự án

<v-clicks>

1. `Ngắn gọn`: Tên nhánh ngắn gọn và mô tả rõ mục đích của nó.
2. `Rõ ràng`: Tên nhánh nên mô tả rõ ràng về nhiệm vụ hoặc tính năng đang phát triển
3. `Tránh kí tự đặc biệt`: Hạn chế sử dụng các kí tự đặc biệt trong tên nhánh để tránh xung đột khi làm việc trên các hệ thống khác nhau
4. `Phân cách bằng dấu gạch ngang hoặc dấu gạch dưới`: Sử dụng `dấu gạch ngang` hoặc `dấu gạch dưới` để phân cách các tên nhánh

</v-clicks>

---

dragPos:
square: 59,143,888,381

---

dragPos:
square: -66,0,0,0

---

dragPos:
square: 63,147,851,368

---

dragPos:
square: -66,0,0,0

---

dragPos:
square: -66,0,0,0

---

dragPos:
square: -66,0,0,0

---

dragPos:
square: -66,0,0,0

---

dragPos:
square: -66,0,0,0

---

dragPos:
square: -71,0,0,0

---

dragPos:
square: -66,0,0,0

# Thực hành

- Tạo repository và thực hiện tạo nhánh sao cho lịch sử như hình. (mỗi nhánh tạo ra 1 file text mới).

<img v-drag="'square'" src="./picture/Practice.png">

---

# Merge Branch

<v-clicks>

- Dùng để hợp nhất các nhánh (branch) khác nhau trong GIT.
- Cú pháp:

```html
git merge ten_chi_dinh
```

- Kết quả:

```sh
PS A:\NET_001\git> git merge br1
Updating 3e31fdf..4122bc5
Fast-forward
 abc.txt | 1 +
 1 file changed, 1 insertion(+)
```

</v-clicks>

---

# Các loại merge

- `Fast-forward merge:` Khi nhánh chính chưa có commit mới nào kể từ khi tách nhánh.
- `Three-way merge:` Khi cả 2 nhánh có thay đổi, Git cần tạo một commit mới để hợp nhất.

---

# Thực hành

1. Tạo repository mới
2. Tạo file abc.txt mới và commit
3. Tạo nhánh mới
4. Thay đổi hoặc thên file mới và commit ở nhánh mới thêm
5. Sử dụng merge
6. Chụp màn hình gửi vào chat

---

# Git clone

<v-clicks>

- Lấy source code từ một repository về máy local

- Cú pháp:

```sh
git clone abcxyx                            #abcxyx đây là link của source code
```

</v-clicks>

---

# Pull Request (Merge Request)

<v-clicks>

- Lấy source mới nhất từ remote repository về máy local.

- Cú pháp:

```html
git pull
```

- Cách hoạt động: Thực hiện 2 thao tác: `git fetch` (tải dữ liệu) và `git merge`.

</v-clicks>

---

# Git push

<v-clicks>

- Đẩy các commit từ local repository lên remote repository

```sh
git push origin ten_nhanh                 #origin là nhánh từ local và ten_nhanh là nhánh từ remote
```

- Lưu ý: Nếu có commit mới trên remote mà chưa có trên local, cần chạy `git pull` trước để tránh conflict

</v-clicks>

---

# Conflict

<v-clicks>

- Nguyên nhân:

  - Hai nhánh chỉnh sửa cùng một dòng cùng một file.
  - Một nhánh xóa file trong khi nhánh khác chỉnh sửa trong file đó.
  - Merge gặp xung đột

- Nhận biết:

```bash
Auto-merging example.txt
CONFLICT (content): Merge conflict in example.txt
Automatic merge failed; fix conflicts and then commit the result.
```

- Hoặc có thể sử dụng `git status` để kiểm tra file bị xung đột.

</v-clicks>

---

# Cách giải quyết

<v-clicks>

- Khi bị conflict, file sẽ có dấu hiệu:

```bash
Head
noi dung
====
noi dung
ten_nhanh
```

- Chỉnh sửa lại nội dung theo mong muốn

- Thêm file vào staged: `git add .`

- Tạo commit để hoàn tất chỉnh sửa conflict: `git commit -m "resolve conflict"`

</v-clicks>

---

# Thực hành

<div>Hãy thử giả lập conflict và sau đó giải quyết conflict đó.</div>

---

# Vim

<v-clicks>

- Khi chạy lệnh `git merge`, nếu xảy ra conflict và bạn nhập `git commit` mà không có `-m`, Git sẽ mở Vim để yêu cầu nhập message.
- Khi chạy lệnh `git rebase`, nếu có conflict, Git có thể mở Vim để chỉnh sửa commit.

```bash
# Please enter the commit message for your merge.
#
# Lines starting with '#' will be ignored, and an empty message aborts the commit.
#
# On branch main
# All conflicts fixed but you are still merging.
#
~
~
~
":"
```

</v-clicks>

---

# Cách thoát Vim

<v-clicks>

- Có 2 cách để thoát khỏi Vim:

```bash
:wq                                                 (Lưu commit message và thoát)
```

```bash
:q!                                                (Thoát mà không lưu)
```

</v-clicks>

---

# The end
