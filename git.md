
# Git

Git to nowoczesny, rozproszony systemem kontroli wersji. Jego popularność w ciągu
ostatnich kilku lat rośnie w ogromnym tempie. Git powstał w 2005 roku dla potrzeb
zarządzania kodem źródłowym jądra systemu Linux 2 . Do połowy roku 2012 liczba
plików kodu źródłowego jądra Linuksa urosła do 39 000 plików, a liczba programi-
stów, którzy wzięli udział w jego tworzeniu, do blisko 10 000 3 . W pierwszym tygo-
dniu czerwca 2012 r. w projekcie tym wprowadzono 400 rewizji.

Głównymi zaletami Gita są jego:
 * lokalność;
 * kontrola spójności danych;
 * optymalizacja pod kątem rozgałęziania;
 * fakt, że jest to system rozproszony;
 * wydajność.

https://git-scm.com/book/pl/v2

## Repozyturium

Git śledzi zmiany plików w obrębie konkretnego folderu. Nie ma znaczenia, czy folder ten zawiera kod źródłowy programu komputerowego, rękopis książki czy stronę WWW. Folder, którego zawartość jest kontrolowana przez Git, będziemy nazywali repozytorium (ang. repository). Repozytoria 4 zawierają specjalny podfolder .git, w którym zapisywane są szczegółowe dane o śledzonych plikach.

### Inicjalizacja nowego repozytorium

```
git init
```
### Klonowanie repozytoriów

```
git clone [adres]
```

## Badanie historii projektu

Do sprawdzania zmian wprowadzonych w repozytorium służy komenda:

```
git log
```

Polecenie git log pozwala filtrować dane oraz formatować sposób prezentacji. Parametr
--pretty ustala domyślny format wydruku. Może on przyjmować wartości:

| Wartość      |       |
|:---------|:-------------|
| oneline | ID rewizji, krótki opis |
|short |format oneline + autor rewizji|
|medium | format short + data rewizji|
|full | format medium bez daty + osoba dołączająca rewizję do projektu|
|fuller | format full + data wykonania rewizji, data dołączenia rewizji|
|email | podstawowe informacje w formacie email|
|raw | informacje dotyczące powiązań rewizji (parent, tree)|
|format | formatowanie zdefiniowane przez użytkownika|
| | |
| -n | liczba interesujących nas rewizji np. –7 oznacza ostatnie 7 rewizji |
| --since="yyyy-mm-dd" | data początkowa|
| --until="yyyy-mm-dd" | data końcowa|
| --author=ktos | rewizje wykonane przez wybranego autora |

# Stany plików

| Rodzaj      |      |  |
|:---------|:-----|:---|
| untracked | nieśledzonymi| zawarty w przestrzeni roboczej, ale nie jest zawarty w repozytorium. Każdy nowo utworzony plik jest nieśledzony aż do momentu wydania komend ```git add``` oraz ```git commit```. |
| unmodified | aktualnymi| zapisany w repozytorium i w przestrzeni roboczej i jego zawartość w obu lokalizacjach jest identyczna. Bezpośrednio po wydaniu komend git add oraz git commit wszystkie pliki są aktualne.  |
| modified | zmodyfikowanymi| plik, którego treść w repozytorium różni się od treści w obszarze roboczym. Jeśli po wydaniu poleceń git add oraz git commit zmienimy treść pliku w obszarze roboczym, to plik ten stanie się zmodyfikowany.  |

# Stan repozytorium
 Do sprawdzania stanu repozytorium służy komenda:
```
git status
```

# Ignorowanie plików

Dla wykluczania plików zawartych w obszarze roboczym z repozytorium trzeba dodać ich do specjalnego pliku _.gitignore_.

### Przykłady

https://github.com/github/gitignore

