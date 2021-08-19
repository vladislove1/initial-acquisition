1) Регистрация на сайте https://thegraph.com/
2) После авторизации перейти https://thegraph.com/legacy-explorer/dashboard, нажать на кнопку "add subgraph", заполнить поля
3) Заходим в cmd/terminal, вводим команду:
```yarn global add @graphprotocol/graph-cli```
или
```yarn global add @graphprotocol/graph-cli```

4) Инициализируем проект сабграфа
```
graph init --product hosted-service <GITHUB_USER>/<SUBGRAPH NAME>
```

    4.1) Указываем имя сабграфа
    4.2) Имя папки
    4.3) сеть - mainnet для eth, bsc для binance
    4.4) Адересс main contract
    4.5) Если Abi не подтянулось автоматически, нужно зайти на сайт https://bscscan.com/ или https://etherscan.io/, выполнить поиск по адрессу контракта, перейти на вкладку Contract, сохранить Abi и указать путь к файлу.
    4.6) Указать имя контракта
5)

