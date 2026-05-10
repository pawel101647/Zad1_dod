# Zad1_dod
Rozwiązanie do zadania 1 - część nieobowiązkowa

# Raport zagrożeń
Rodzaje zagrożeń w obrazie: <br>
<img width="1870" height="723" alt="image" src="https://github.com/user-attachments/assets/7b11ebf0-405c-4b4a-9979-0755851f7d24" />
<br>
Zagrożenie zakwalifikowane jako "High": <br>
<img width="1913" height="1027" alt="image" src="https://github.com/user-attachments/assets/7fe7fa92-b9f3-489a-8761-be92c5825aff" />
<br>
Podatność CVE dotycząca curl (use-after-free w obsłudze SMB connection reuse) nie stanowi realnego zagrożenia w aplikacji, ponieważ kontener nie wykorzystuje protokołu SMB ani funkcjonalności curl związanych z tym protokołem. Aplikacja wykonuje jedynie zapytania HTTP, dlatego podatność nie jest możliwa do wykorzystania w tym środowisku.

# Użyte polecenia
Utworzenie i uruchomienie buildera: "docker buildx create --driver docker-container --name mybuilder --use --bootstrap" <br>
Po uruchomieniu polecenia stworzony został builder, a następnie oznaczony jako aktywny. <br><br>
Zbudowanie obrazu dla dwóch platform: "docker buildx build -q -t pawel19/repo1:zad1.v2 --platform linux/amd64,linux/arm64 --push ." <br>
Sprawdzenie manifestu: "docker buildx imagetools inspect pawel19/repo1:zad1.v2" <br>
Po wpisaniu polecenia można zobaczyć platformy: linux/amd64 oraz linux/arm64. <br>
<img width="1206" height="337" alt="image" src="https://github.com/user-attachments/assets/cfed3a1b-cefa-4f8d-bd5f-d7352b6109ba" />
