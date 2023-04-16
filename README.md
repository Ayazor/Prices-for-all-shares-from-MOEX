# Информация по всем акциям за весь возможный период с API MOEX
Данный проект предназанчен для тех, кому нужны цены акций с Московской биржи за весь период, который только возможно выгрузить с API MOEX.

Главный файл - это csv файл "Данные по всем акциям.csv", в котором и хранятся цены по всем акциям с API MOEX.
В нем много Nan строк, т.к. я решил взять дату с 01.01.2000 года, чтобы получить цены по всевозможным датам. Т.к. целью этого датафрейма является получение определенных данных за определенный период, то данные строки никак не мешают и являются лишь неким ориентиром.

Стоит отметить, что csv-файл содежит около 500 компаний в отличие от файла со списком компаний. Но это потому что на многие запросы API MOEX не мог ответить, т.к. информации по акциям не было.

В папке "Методика получения цены акций" дан код, с помощью которого и был получен главный csv-файл. Также в этой папке есть еще 2 файла. Один из них - "Chageover". В нем указаны все изменения тикеров компаний, которые произошли. Второй файл с наименованием всех акций, которые когда-либо были на Мосбирже.
Стоит отметить, что не по всем акциям из данного файла есть информация с API, поэтому колонок в финальной файле меньше.

Также IPYNB-файл "Функция получения цены акции" предназначена для того, чтобы извлекать датафрейм из csv-файла со всеми ценами для дальнейшей работы.
В качестве аргументов у нее список компаний, данные по которым вы хотите получить и дата начала и конца желаемого периода. Также в нем приведен пример получения датафрейма для акций Газпрома.
