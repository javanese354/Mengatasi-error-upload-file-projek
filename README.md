# Mengatasi-error-upload-file-projek
Mengatasi error saat upload file projek ke Github dengan Git Bash

Banyak cara untuk upload file projek ke Repository Github, ada yang pake Github Windows, tapi banyak juga yang pake Git Bash, 
yang suka pake command line pasti sukanya upload pake Git Bash, tapi...

Pernah gak kaliah mengalami error saat upload file projek ke Repository Github ?
biasanya untuk orang yang baru pertama kali upload pasti mengalami error ini

>! [rejected] master -> master (non-fast-forward)
error: failed to push some refs to 'https://github.com/example/example.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.>hint: See the 'Note about fast-forwards' in 'git push --help' for details.

nah, mudah ni cara mengatasinya, cukup ikuti langkah berikut ini :
1. Buat dulu Repository kalian
2. Buka Git Bash kalian dan ketik perintah berikut
 $ git init
 
 $ git add .
 
 $ git commit -m "First commit"
 
 $ git remote add origin {remote repository URL} 
 
 contoh git remote add origin https://github.com/example/example.git
 
 Solusinya ada di sini nih,
 
 Solusinya tambahkan tag --allow-unrelated-histories // tapi hanya sekali saja, kalo mau upload projek baru, tidak perlu ketik lagi, langsung ketik perintah $ git pull origin master 
 
 $ git pull origin master --allow-unrelated-histories
 
 Habis itu, baru deh kalian Push
 
 $ git push origin master

# Selamat Mencoba
