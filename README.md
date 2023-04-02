# setup-vm-nstanceGC

    node -v
    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash
    reboot
    nvm ls-remote
    nvm install v18.14.1
    
    melihat git sudah terinstall
    sudo git -v
    sudo apt-get install git
    mkdir web-nuxt
    cd web-nuxt
    git clone https://github.com/zulfahmidev/projek_todolist.git
    
    cd projek_todolist/
    npm install
    npm run dev //untuk debug
    npm run build
    npm run preview 





buat image untuk projek

buat file Dockerfile pada projek

        FROM node:18.14.1-alpine
        WORKDIR /app
        COPY . /app
        RUN npm install
        RUN npm run build
        EXPOSE 3000
        CMD [ "npm", "run", "preview"]
        
lalu simpan file sebelum build image pastikan untuk menhapus node_moduls pada projek

lalu jalan kan perintah berikut

        docker build -t web-nuxt:1.0 .   //tunggu sampai selesai
        
        docker container run -d -p 3001:3000 sepol123/projek_web_nuxtjs:0.0.1.RELEASE // menjalankan container dari image yang kita buat
        docker push sepol123/projek_web_nuxtjs:0.0.1.RELEASE // untuk push image ke docker hub
        
