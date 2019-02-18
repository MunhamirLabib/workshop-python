# minggu-11

Flask adalah kerangka (framework) Python untuk membuat aplikasi web. Dari situs aslinya,
Flask adalah microframework untuk Python berbasis Werkzeug, Jinja 2 dan "niat baik".
Ketika kita memikirkan Python, kerangka de facto yang muncul di benak kita adalah framework Django. Tapi dari perspektif pemula Python, Flask lebih mudah, jika dibandingkan dengan Django.
Menyiapkan Flask
Menyiapkan Flask sangat sederhana dan cepat. Dengan package manager pip, semua yang perlu kita lakukan adalah:
1	pip install flask
Setelah anda selesai meng-install Flask, buat folder dengan nama FlaskApp. Masuk ke folder FlaskApp dan buat sebuah file dengan nama app.py. Import modul flask dan buat aplikasi menggunakan Flask seperti ditunjukkan berikut:
1
2	from flask import Flask
app = Flask(__name__)
Sekarang tentukan basic route / dan handler yang sesuai:
1
2
3	@app.route("/")
def main():
    return "Welcome!"
Berikutnya, periksa jika file yang dieksekusi adalah program utama dan jalankan app-nya
1
2	if __name__ == "__main__":
    app.run()
Simpan perubahan dan eksekusi app.py:
1	python app.py
Arahkan browser Anda ke http://localhost: 5000/ dan Anda pasti memiliki pesan pembuka, "welcome".
Membuat Home Page
Pertama, ketika aplikasi berjalan kita akan menampilkan home page dengan isi dari daftar keinginan terbaru yang ditambahkan oleh pengguna. Jadi, mari menambahkan home page ke folder aplikasi kita.
Flask mencari file template di dalam folder templates. Jadi, navigasi ke folder PythonApp dan buat folder dengan nama templates. Didalam templates, buat sebuah file dengan nama index.html. Buka index.htmldan tambahkan HTML.
<!DOCTYPE html>
<html lang="en">
 
<head>
    <title>Python Flask Bucket List App</title>
 
 
    <link href="http://getbootstrap.com/dist/css/bootstrap.min.css" rel="stylesheet">
 
    <link href="http://getbootstrap.com/examples/jumbotron-narrow/jumbotron-narrow.css" rel="stylesheet">
 
 
</head>
 
<body>
 
    <div class="container">
        <div class="header">
            <nav>
                <ul class="nav nav-pills pull-right">
                    <li role="presentation" class="active"><a href="#">Home</a>
                    </li>
                    <li role="presentation"><a href="#">Sign In</a>
                    </li>
                    <li role="presentation"><a href="showSignUp">Sign Up</a>
                    </li>
                </ul>
            </nav>
            <h3 class="text-muted">Python Flask App</h3>
        </div>
 
        <div class="jumbotron">
            <h1>Bucket List App</h1>
            <p class="lead"></p>
            <p><a class="btn btn-lg btn-success" href="showSignUp" role="button">Sign up today</a>
            </p>
        </div>
 
        <div class="row marketing">
            <div class="col-lg-6">
                <h4>Bucket List</h4>
                <p>Donec id elit non mi porta gravida at eget metus. Maecenas faucibus mollis interdum.</p>
 
                <h4>Bucket List</h4>
                <p>Morbi leo risus, porta ac consectetur ac, vestibulum at eros. Cras mattis consectetur purus sit amet fermentum.</p>
 
                <h4>Bucket List</h4>
                <p>Maecenas sed diam eget risus varius blandit sit amet non magna.</p>
            </div>
 
            <div class="col-lg-6">
                <h4>Bucket List</h4>
                <p>Donec id elit non mi porta gravida at eget metus. Maecenas faucibus mollis interdum.</p>
 
                <h4>Bucket List</h4>
                <p>Morbi leo risus, porta ac consectetur ac, vestibulum at eros. Cras mattis consectetur purus sit amet fermentum.</p>
 
                <h4>Bucket List</h4>
                <p>Maecenas sed diam eget risus varius blandit sit amet non magna.</p>
            </div>
        </div>
 
        <footer class="footer">
            <p>&copy; Company 2015</p>
        </footer>
 
    </div>
</body>
 
</html>
Buka app.py dan import render_template, dimana kita akan menggunakan untuk me-render file-file template.
1	from flask import Flask, render_template
Ubah metode utama untuk mengembalikan file template yang di-render.
1
2	def main():
    return render_template('index.html')
