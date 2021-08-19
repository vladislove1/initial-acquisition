1) Регистрация на сайте https://thegraph.com/
2) После авторизации перейти https://thegraph.com/legacy-explorer/dashboard, нажать на кнопку "add subgraph", заполнить поля
3) Заходим в cmd/terminal, вводим команду:
```
yarn global add @graphprotocol/graph-cli
```
или
```
yarn global add @graphprotocol/graph-cli
```

4) Инициализируем проект сабграфа
```
graph init --product hosted-service <GITHUB_USER>/<SUBGRAPH NAME>

    4.1) Указываем имя сабграфа
    4.2) Имя папки
    4.3) сеть - mainnet для eth, bsc для binance
    4.4) Адересс main contract
    4.5) Если Abi не подтянулось автоматически, нужно зайти на сайт https://bscscan.com/ или https://etherscan.io/, выполнить поиск по адрессу контракта, перейти на вкладку Contract, сохранить Abi и указать путь к файлу.
    4.6) Указать имя контракта
5) Ввести команду `graph auth --product hosted-service <ACCESS_TOKEN>` Token можно найти на странице сабграфа
6) Для деплоя нужно сгенеривровать graphql модели и типы с помощью команды `yarn codegen` и выполнить команду `yarn deploy`
Для разработки необходимо установить старотовый блок, с которого сабграф будет начинать обрабатывать информацию, Для этого в файл `subgraph.yaml` нужно добавить номер блока нужного нам блока
```dataSources:
  - kind: ethereum/contract
    name: Contract
    network: mainnet
    source:
      address: "0xEEA92913d8AA554a102ED5B4F0A6206E6D8d59D5"
      abi: Contract
      >>startBlock: 12737701```

