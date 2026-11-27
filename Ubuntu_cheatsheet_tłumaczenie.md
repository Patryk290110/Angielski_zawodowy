**Canonical Ubuntu | Ściągawka Ubuntu CLI**

---

### Strona 1

# System

**Informacje o systemie**  
`uname -a` Wyświetla wszystkie informacje o systemie.  
`hostnamectl` Pokazuje bieżącą nazwę hosta i powiązane szczegóły.  
`lscpu` Wyświetla informacje o architekturze CPU.  
`timedatectl status` Pokazuje czas systemowy.  

**Monitorowanie i zarządzanie systemem**  
`top` Wyświetla procesy systemowe w czasie rzeczywistym.  
`htop` Interaktywna przeglądarka procesów (wymaga instalacji).  
`df -h` Pokazuje użycie dysku w formacie czytelnym dla człowieka.  
`free -m` Wyświetla wolną i zajętą pamięć w MB.  
`kill <id procesu>` Kończy proces.  

**Uruchamianie poleceń**  
`<polecenie> &` Uruchamia polecenie w tle.  
`jobs` Wyświetla polecenia działające w tle.  
`fg <numer polecenia>` Przenosi polecenie na pierwszy plan.  

**Zarządzanie usługami**  
`sudo systemctl start <usługa>` Uruchamia usługę.  
`sudo systemctl stop <usługa>` Zatrzymuje usługę.  
`sudo systemctl status <usługa>` Sprawdza status usługi.  
`sudo systemctl reload <usługa>` Przeładowuje konfigurację usługi bez przerywania jej działania.  
`journalctl -f` Śledzi dziennik, pokazując nowe komunikaty dziennika w czasie rzeczywistym.  
`journalctl -u <nazwa_jednostki>` Wyświetla dzienniki dla określonej jednostki systemd.  

**Zadania cron i planowanie**  
`crontab -e` Edytuje zadania cron dla bieżącego użytkownika.  
`crontab -l` Wyświetla listę zadań cron dla bieżącego użytkownika.  

# Pliki

**Zarządzanie plikami**  
`ls` Wyświetla listę plików i katalogów.  
`touch <nazwa_pliku>` Tworzy pusty plik lub aktualizuje datę ostatniego dostępu.  
`cp <źródło> <cel>` Kopiuje pliki ze źródła do miejsca docelowego.  
`mv <źródło> <cel>` Przenosi pliki lub zmienia ich nazwy.  
`rm <nazwa_pliku>` Usuwa plik.  

**Nawigacja po katalogach**  
`pwd` Wyświetla ścieżkę bieżącego katalogu.  
`cd <katalog>` Zmienia bieżący katalog.  
`mkdir <nazwa_katalogu>` Tworzy nowy katalog.  

**Uprawnienia do plików i własność**  
`chmod [kto][+/-][uprawnienia] <plik>` Zmienia uprawnienia pliku.  
`chmod u+x <plik>` Nadaje plikowi prawo wykonywania przez jego właściciela.  
`chown [użytkownik]:[grupa] <plik>` Zmienia właściciela i grupę pliku.  

**Wyszukiwanie i znajdowanie**  
`find [katalog] -name <wzorzec_wyszukiwania>` Znajduje pliki i katalogi.  
`grep <wzorzec_wyszukiwania> <plik>` Wyszukuje wzorzec w plikach.  

**Archiwizacja i kompresja**  
`tar -czvf <nazwa.tar.gz> [pliki]` Kompresuje pliki do archiwum tar.gz.  
`tar -xvf <nazwa.tar.[gz|bz|xz]> [cel]` Rozpakowuje skompresowane archiwum tar.  

**Edycja i przetwarzanie tekstu**  
`nano <plik>` Otwiera plik w edytorze tekstu Nano.  
`cat <plik>` Wyświetla zawartość pliku.  
`less <plik>` Wyświetla zawartość pliku w formie stronicowanej.  
`head <plik>` Pokazuje kilka pierwszych linii pliku.  
`tail <plik>` Pokazuje kilka ostatnich linii pliku.  
`awk '{print}' <plik>` Wypisuje każdą linię w pliku.  

---

### Strona 2

# Pakiety

**Zarządzanie pakietami (APT)**  
`sudo apt install <pakiet>` Instaluje pakiet.  
`sudo apt install -f --reinstall <pakiet>` Reinstaluje uszkodzony pakiet.  
`apt search <pakiet>` Wyszukuje pakiety APT.  
`apt-cache policy <pakiet>` Wyświetla dostępne wersje pakietu.  
`sudo apt update` Aktualizuje listy pakietów.  
`sudo apt upgrade` Aktualizuje wszystkie pakiety możliwe do zaktualizowania.  
`sudo apt remove <pakiet>` Usuwa pakiet.  
`sudo apt purge <pakiet>` Usuwa pakiet oraz wszystkie jego pliki konfiguracyjne.  

**Zarządzanie pakietami (Snap)**  
`snap find <pakiet>` Wyszukuje pakiety Snap.  
`sudo snap install <nazwa_snapa>` Instaluje pakiet Snap.  
`sudo snap remove <nazwa_snapa>` Usuwa pakiet Snap.  
`sudo snap refresh` Aktualizuje wszystkie zainstalowane pakiety Snap.  
`snap list` Wyświetla wszystkie zainstalowane pakiety Snap.  
`snap info <nazwa_snapa>` Wyświetla informacje o pakiecie Snap.  

# Użytkownicy i grupy

**Zarządzanie użytkownikami**  
`w` Pokazuje, którzy użytkownicy są zalogowani.  
`sudo adduser <nazwa_użytkownika>` Tworzy nowego użytkownika.  
`sudo deluser <nazwa_użytkownika>` Usuwa użytkownika.  
`sudo passwd <nazwa_użytkownika>` Ustawia lub zmienia hasło użytkownika.  
`su <nazwa_użytkownika>` Przełącza użytkownika.  
`sudo passwd -l <nazwa_użytkownika>` Blokuje konto użytkownika.  
`sudo passwd -u <nazwa_użytkownika>` Odblokowuje hasło użytkownika.  
`sudo chage <nazwa_użytkownika>` Ustawia datę wygaśnięcia hasła użytkownika.  

**Zarządzanie grupami**  
`id [nazwa_użytkownika]` Wyświetla identyfikatory (ID) użytkownika i grup.  
`groups [nazwa_użytkownika]` Pokazuje grupy, do których należy użytkownik.  
`sudo addgroup <nazwa_grupy>` Tworzy nową grupę.  
`sudo delgroup <nazwa_grupy>` Usuwa grupę.  

# Sieć

**Sieć**  
`ip addr show` Wyświetla interfejsy sieciowe i adresy IP.  
`ip -s link` Pokazuje statystyki sieciowe.  
`ss -l` Pokazuje gniazda nasłuchujące.  
`ping <host>` Wysyła żądanie ping do hosta i wyświetla wyniki.  

**Konfiguracja Netplan (więcej informacji na netplan.io)**  
`cat /etc/netplan/*.yaml` Wyświetla bieżącą konfigurację Netplan.  
`sudo netplan try` Testuje nową konfigurację przez określony czas.  
`sudo netplan apply` Stosuje bieżącą konfigurację Netplan.  

**Zarządzanie zaporą sieciową**  
`sudo ufw status` Wyświetla status zapory sieciowej.  
`sudo ufw enable` Włącza zaporę sieciową.  
`sudo ufw disable` Wyłącza zaporę sieciową.  
`sudo ufw allow <port/usługa>` Zezwala na ruch na określonym porcie lub dla określonej usługi.  
`sudo ufw deny <port/usługa>` Blokuje ruch na określonym porcie lub dla określonej usługi.  
`sudo ufw delete allow/deny <port/usługa>` Usuwa istniejącą regułę.  

**SSH i dostęp zdalny**  
`ssh <użytkownik@host>` Łączy się ze zdalnym hostem przez SSH.  
`scp <źródło> <użytkownik@host>:<cel>` Bezpiecznie kopiuje pliki między hostami.  

---

### Strona 3

# LXD

LXD to nowoczesne, bezpieczne i potężne narzędzie zapewniające ujednolicone środowisko do uruchamiania kontenerów lub maszyn wirtualnych oraz zarządzania nimi. Odwiedź stronę canonical.com/lxd, aby uzyskać więcej informacji.

`lxd init` inicjalizuje LXD przed pierwszym użyciem  

**Tworzenie instancji**  
`lxc init ubuntu:24.04 <nazwa kontenera>` Tworzy kontener systemowy lxc (bez uruchamiania go).  
`lxc launch ubuntu:24.04 <nazwa kontenera>` Tworzy i uruchamia kontener systemowy lxc.  
`lxc launch ubuntu:24.04 <nazwa vm> --vm` Tworzy i uruchamia maszynę wirtualną.  

**Zarządzanie instancjami**  
`lxc list` Wyświetla listę instancji.  
`lxc info <instancja>` Pokazuje informacje o stanie instancji.  
`lxc start <instancja>` Uruchamia instancję.  
`lxc stop <instancja> [--force]` Zatrzymuje instancję.  
`lxc delete <instancja> [--force|--interactive]` Usuwa instancję.  

**Dostęp do instancji**  
`lxc exec <instancja> -- <polecenie>` Uruchamia polecenie wewnątrz instancji.  
`lxc exec <instancja> -- bash` Uzyskuje dostęp do powłoki instancji (jeśli zainstalowano bash).  
`lxc console <instancja> [flagi]` Uzyskuje dostęp do konsoli instancji.  
`lxc file pull <instancja>/<ścieżka_pliku_w_instancji> <lokalna_ścieżka_pliku>` Pobiera plik z instancji.  
`lxc file push <lokalna_ścieżka_pliku> <instancja>/<ścieżka_pliku_w_instancji>` Wysyła plik do instancji.  

**Korzystanie z projektów**  
`lxc project create <projekt> [--config <opcja>]` Tworzy projekt.  
`lxc project set <projekt> <opcja>` Konfiguruje projekt.  
`lxc project switch <projekt>` Przełącza na projekt.  

# Ubuntu Pro

Ubuntu Pro zapewnia do 12 lat wsparcia w zakresie bezpieczeństwa, rozszerzając zobowiązanie Long Term Support (LTS) systemu Ubuntu oraz dodając narzędzia do zarządzania i zapewniania zgodności. Odwiedź stronę ubuntu.com/pro, aby zarejestrować się za darmo na maksymalnie pięciu maszynach.

**Aktywacja Ubuntu Pro**  
`sudo pro attach <token>` Podłącza maszynę do Ubuntu Pro za pomocą określonego tokena. Token ten jest dostarczany po wykupieniu subskrypcji Ubuntu Pro.  

**Zarządzanie usługami**  
`sudo pro status` Wyświetla status wszystkich usług Ubuntu Pro.  
`sudo pro enable <usługa>` Włącza określoną usługę Ubuntu Pro, taką jak ESM, FIPS lub Livepatch.  
`sudo pro disable <usługa>` Wyłącza określoną usługę Ubuntu Pro.  

**Rozszerzone utrzymanie bezpieczeństwa (ESM)**  
`sudo pro enable esm-infra` Aktywuje Extended Security Maintenance dla pakietów infrastruktury, zapewniając aktualizacje bezpieczeństwa poza standardowym cyklem wydawniczym.  
`sudo pro enable esm-apps` Aktywuje ESM dla aplikacji, rozszerzając ochronę bezpieczeństwa na określone aplikacje.  

**Usługa Livepatch**  
`sudo pro enable livepatch` Włącza usługę Livepatch, która stosuje krytyczne łatki jądra bez ponownego uruchamiania systemu.  

**Tryb FIPS**  
`sudo pro enable fips` Włącza tryb FIPS (Federal Information Processing Standards), wymuszając rygorystyczne standardy i praktyki kryptograficzne.  

**Aktualizacja konfiguracji**  
`sudo pro refresh` Odświeża stan Ubuntu Pro, aby upewnić się, że zastosowano najnowszą konfigurację i usługi.  

**Odłączanie Ubuntu Pro**  
`sudo pro detach` Odłącza maszynę od Ubuntu Pro, wyłączając wszystkie usługi.