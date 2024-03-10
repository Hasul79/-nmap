# Шпаргалка по nmap

<ol>
  <li>
  
```
nmap  [Target]

```
    
   nmap 192.168.0.1 - простое сканирование, с 1 по 1000 порт   
    </li>
       <br/>
<li>
  
```
nmap -p- [Target]

```

 Сканирование всех портов (полный диапазон):
 </li>
 <br/>
 <li>

   ```
nmap -p 1-100 [Target]

```
nmap -p 100-25525 192.168.0.1-10 - указываем диапазон портов и IP-адресов (nmap -p 80, nmap -p "*")
</li>
<br/>
<li>
  
  ```
nmap --top-ports 100 <target>

```
nmap --top-ports 10 192.168.0.1 - сканируем топовые порты</li>
<li>
  
  ```
nmap -Pn <target>

```
nmap -Pn 192.168.0.1 - сканируем без пинга
</li>
<br
  
<li>
  
  ```

nmap -O [Target]

```
nmap -O 192.168.0.1 - определение ОС
</li>
<br/>
<li>nmap -sV 192.168.0.1 - пытаемся узнать, что за сервисы запущены на открытых портах</li>
<li>nmap –sP 192.168.0/24 - пинг-сканирование</li>
<li>
  
  ```
nmap -sn [Target]

```
nmap -sn 192.168.1.0/24 - ищем активные хосты</li>
<li>nmap -sO 192.168.0.1 - определяем поддерживаемые протоколы</li>

<li>nmap -sT 192.168.0.1 - сканируем все TCP-порты</li>
<li>nmap -p T:80 192.168.0.1 - определенный TCP-порт</li>
<br>
<li>
  
  ```
  nmap -p- --open [Target]

  ```
--open: Показывать только открытые порты.
</li>
<br>
<li>
  
  ```
nmap -sU [Target]

```
nmap -sU 192.168.0.1 - сканируем UDP-порты (nmap -p U:53)</li>
<br>
<li>

  ```
nmap -A [Target]

```
<p>Версия сервисов и операционной системы: </p>
-A: Включение опций определения версий и ОС.
<br/>
</li>
<br/>
<li>

  ```
nmap --proxy [ProxyIP:ProxyPort] [Target]

```
<p>Сканирование с прокси:</p>
--proxy: Указание прокси-сервера для сканирования.
<br/>
</li>
<br/>
<li>

  ```
nmap -oN output.txt [Target]

```
<p>Сохранение результатов в файл:</p>
-oN output.txt: Сохранение результатов в текстовый файл.

</li>
<br>
<li>nmap -sA 192.168.0.1 - определяем, есть ли файервол</li>

<li>nmap -sS 192.168.0.1 - скрытое сканирование</li>
</ol> 
