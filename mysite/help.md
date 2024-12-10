Chúng ta sẽ tạo một virtualenv có tên là myvenv. Lệnh chung sẽ có định dạng:
    py -m venv myvenv  
Bắt đầu môi trường ảo của bạn bằng cách chạy: 
    myvenv\Scripts\activate
Trước khi thực hiện, chúng ta nên đảm bảo rằng mình có phiên bản mới nhất của pipphần mềm mà chúng ta sử dụng để cài đặt Django:
    py -m pip install --upgrade pip

Bạn cần phải ở trong thư mục chứa manage.pytệp ( djangogirlsthư mục). Trong bảng điều khiển, chúng ta có thể khởi động máy chủ web bằng cách chạy 
    py manage.py runserver

##### When you install Django on your computer, everything works fine but when you install a Virtual environment it gets separated from all things. You will know it's importance when you will make a final project and deploy it to any cloud or hosting.

##### Just re-install Django in the virtual environment and baam:

pip install Django
and then just run the command for testing:

python manage.py runserver
and you are all done.
##### 

#Để tạo cơ sở dữ liệu cho blog của chúng ta, hãy chạy lệnh sau trong bảng điều khiển: 
    py manage.py migrate

Để tạo một ứng dụng, chúng ta cần chạy lệnh sau trong bảng điều khiển 
    py manage.py startapp blog

Đầu tiên, chúng ta phải cho Django biết rằng chúng ta có một số thay đổi trong mô hình của mình. (Chúng ta vừa tạo nó!) Vào cửa sổ bảng điều khiển của bạn và nhập 
    py manage.py makemigrations blog

py manage.py createsuperuser


Bây giờ chúng ta cần kết nối kho lưu trữ Git trên máy tính của bạn với kho lưu trữ trên GitHub.

Nhập nội dung sau vào bảng điều khiển của bạn (thay thế <your-github-username>bằng tên người dùng bạn đã nhập khi tạo tài khoản GitHub, nhưng không có dấu ngoặc nhọn -- URL phải khớp với URL bản sao mà bạn vừa thấy).

 git remote add origin https://github.com/JanKKaa/my-first-blog.git
 git push -u origin HEAD
  This works for me to override all local changes and does not require an identity:

   git reset --hard
   git pull

Để cài đặt Bootstrap, hãy mở .htmltệp của bạn trong trình soạn thảo mã và thêm nội dung sau vào <head>phần này:
   <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">

