Пример кода, описанный [в данной статье](https://www.digitalocean.com/community/tutorials/nodejs-server-sent-events-build-realtime-app)

1. Запустить сервер  
    ```
    cd sse-server 
    npm i
    node server.js
    ```
   Сервер запустится на http://localhost:3001/
   

2. Запустить клиент

    ```
    cd ../sse-client  
    npm i  
    npm start  
    ```
    Открыть клиент http://localhost:3000/


3. Отправить сообщение 

    ```
   curl -X POST \
    -H "Content-Type: application/json" \
    -d '{"info": "Shark teeth are embedded in the gums rather than directly affixed to the jaw, and are constantly replaced throughout life.", "source": "https://en.wikipedia.org/wiki/Shark"}'\
    -s http://localhost:3001/fact
    ```


4. Проверить, что на клинте обновился список
