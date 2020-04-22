# CeneoScraper12
## Etap 1 - pobranie składowych pojedynczej opinii
- opinia: li.review-box
- identyfikator: li.review-box["data-entry-id"]
- autor: div.reviewer-name-line
- rekomendacja: div.product-review-summary > em
- gwiazdki: span.review-score-count
- potwierdzona zakupem: div.product-review-pz
- data wystawienia: span.review-time > time["datetime"] - pierwszy element listy
- data zakupu: span.review-time > time["datetime"] - drugi element listy
- przydatna: span[id=^vote-yes]
             button.vote-yes["data-total-vote"]
             button.vote-yes > span
- nieprzydatna: span[id=^vote-no]
             button.vote-no["data-total-vote"]
             button.vote-no > span
- treść: p.product-review-body
- wady: div.cons-cell > ul
- zalety: div.pros-cell > ul

## Etap 2 - pobranie składowych wszystkich opinii z pojedynczej strony
- zapisanie składowych opinii w złozonej strukturze danych
## Etap 3 - pobranie wszystkich opinii o pojedynczym produkcie
- przechodzenie po stronach z opiniami
- eksport opinii do pliku (.csv lub .xlsx lub .json)
## Etap 4
- transformacja danych
- refaktoryzacja kodu

## Etap 5
- zapis danych do obiektu dataframe (ramka danych)
- wykonanie podstawowych obliczeń na danych w ramce danych
- wykonanie prostych wykresów na podstawie danych

## Etap 6 - przygotowanie interfejsu webowego aplikacji (Flask)
- struktura aplikacji
    /CeneoScraper
        /yourapp
            /run.py
            /config.py
            /app
                /__init__.py
                /views.py
                /models.py
                /scraper.py
                /analyzer.py
                /opinions_json
                /static/
                    /main.css
                /templates/
                    /layout.html
                /requirements.txt
                /README.md
                /.venv
- widoki (Jinja)
- routingi