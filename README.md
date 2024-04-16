# 1440 Test Task

Запуск API:
python start_api.py

<details>
<summary> Список эндпойнтов. </summary>

1. Выполнить соединение с сокетом-сервером(источником питания).

    ```
    GET /connect
    ```

2. Опрос телеметрии источника питания.

    ```
    GET /telemetry/<channel>
    ```
    Метод принимает номер канала и возвращает ответ с кодом `200` и данные телеметрии(напряжение, ток, мощность) с этого канала.

3. Запрос текущего состояния всех каналов питания.
  
    ```
    GET /current_state
    ```
    Метод возвращает ответ с кодом `200` и данные в json формате напряжений и токов со всех каналов.

4. Включение канала питания.
  
    ```
    POST /channel/on
    ```
    Метод отправляет команду на выставление указанного тока и напряжения указанного канала, включение канала питания.

5. Включение канала питания.
  
    ```
    POST /channel/off/<channel>
    ```
    Метод отправляет команду отключение указанного канала питания.

