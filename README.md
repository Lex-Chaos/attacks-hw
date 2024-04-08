# Домашняя работа к занятию «Уязвимости и атаки на информационные системы» - Боровик А. А.

### Задание 1

Ответ:

Разрешены следующие сетевые службы:

![Разрешённые службы](https://github.com/Lex-Chaos/attacks-hw/blob/main/img/Task1_Services.png)

Обнаружены следующие уязвимости:

1. vsftpd 2.3.4 - Backdoor Command Execution - [vsftpd 2.3.4 - Backdoor Command Execution - Unix remote Exploit](https://www.exploit-db.com/exploits/49757)
2.  PostgreSQL 8.2/8.3/8.4 - UDF for Command Execution - [PostgreSQL 8.2/8.3/8.4 - UDF for Command Execution - Linux local Exploit](https://www.exploit-db.com/exploits/7855)
3.  ISC BIND 9 - Denial of Service - [ISC BIND 9 - Denial of Service - Multiple dos Exploit](https://www.exploit-db.com/exploits/40453)
4. Samba 3.5.0 - Remote Code Execution - [ISC BIND 9 - Denial of Service - Multiple dos Exploit](https://www.exploit-db.com/exploits/40453)

---

### Задание 2

Ответ:

С точки зрения сетевого трафика отличаются протоколами (TCP/UDP) и флагами посылки запроса и ответа.

Сервер на разные типы сканирования отвечает различными обратными посылками в зависимости от того, закрыт или открыт порт.

SYN сканирование: Сканер посылает запросы SYN на порты санируемого, сканируемый отвечает открытым портом \[SYN, AKC\], закрытым портом \[RST, ACK\]

FIN сканирование: Сканер отправляет запросы FIN на порты сканируемого, сканируемый отвечает закрытым портом \[RST, ACK\], открытым не отвечает.

Xmas сканирование: Сканер отправляет запросы \[FIN, PSH, URG\] на порты сканируемого, сканируемый отвечает закрытым портом \[RST, ACK\], открытым не отвечает.

UDP сканирование: Сканер отправляет UDP пакеты на порты сканируемого, сканируемый отвечает ICMP сообщением об ошибке если порт открыт, если порт закрыт — не отвечает.

Ссылки на файлы записи сеансов сканирования:

[SYN](https://github.com/Lex-Chaos/attacks-hw/blob/main/files/SYN.pcapng)

[FIN](https://github.com/Lex-Chaos/attacks-hw/blob/main/files/FIN.pcapng)

[Xmas](https://github.com/Lex-Chaos/attacks-hw/blob/main/files/Xmas.pcapng)

[UDP](https://github.com/Lex-Chaos/attacks-hw/blob/main/files/UDP.pcapng)
