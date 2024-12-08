    py manage.py runserver

#Để tạo cơ sở dữ liệu cho blog của chúng ta, hãy chạy lệnh sau trong bảng điều khiển: 
    py manage.py migrate

Để tạo một ứng dụng, chúng ta cần chạy lệnh sau trong bảng điều khiển 
    py manage.py startapp blog

Đầu tiên, chúng ta phải cho Django biết rằng chúng ta có một số thay đổi trong mô hình của mình. (Chúng ta vừa tạo nó!) Vào cửa sổ bảng điều khiển của bạn và nhập 
    py manage.py makemigrations blog

py manage.py createsuperuser