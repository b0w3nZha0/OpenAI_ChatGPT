docker cp Nginx:/etc/nginx/nginx.conf 'G:/IntelliJ Workspace/OpenAI_ChatGPT/dev-ops/nginx/conf'
docker cp Nginx:/etc/nginx/conf.d/default.conf 'G:/IntelliJ Workspace/OpenAI_ChatGPT/dev-ops/nginx/conf/conf.d/default.conf'
docker cp Nginx:/usr/share/nginx/html/index.html 'G:/IntelliJ Workspace/OpenAI_ChatGPT/dev-ops/nginx/html'

docker run --name Nginx -p 80:80 -v G:/JavaPersonalProject/OpenAI_ChatGPT/dev-ops/nginx/logs:/var/log/nginx -v G:/JavaPersonalProject/OpenAI_ChatGPT/dev-ops/nginx/html:/usr/share/nginx/html -v G:/JavaPersonalProject/OpenAI_ChatGPT/dev-ops/nginx/conf.d:/etc/nginx/nginx.d -v G:/JavaPersonalProject/OpenAI_ChatGPT/dev-ops/nginx/conf/nginx.conf:/etc/nginx/nginx.conf -d --restart always nginx
