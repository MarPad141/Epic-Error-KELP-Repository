# Webshare.cz

Doplněk pro české cloudové úložiště [Webshare.cz](https://webshare.cz). Umožňuje vyhledávání a streamování video souborů přímo z aplikace StreamujTo.

## Požadavky

- **VIP účet** na [webshare.cz](https://webshare.cz) (s free účtem streamování nefunguje)

## Funkce

- ✅ Přihlášení uživatelským jménem / e-mailem + heslem
- ✅ Vyhledávání video souborů
- ✅ Přímé streamovací odkazy (HTTPS)
- ✅ Automatická kontrola platnosti session
- ✅ Bezpečné hashování hesla (md5crypt + SHA-1)

## Instalace

### Import z URL

1. Otevřete StreamujTo → **Nastavení** → **Doplňky úložišť**
2. Klepněte na **+ Přidat** → **Zadat URL adresu**
3. Vložte URL kterou najdete na webu výše a potvrďte

### Po instalaci

1. Otevřete detail doplňku v nastavení
2. Vyplňte **uživatelské jméno** (nebo e-mail) a **heslo**
3. Klepněte na **Přihlásit se**

## Technické detaily

| Vlastnost | Hodnota |
|-----------|---------|
| ID | `webshare` |
| Typ | `api` (XML REST API) |
| Auth | `credentials` (username + password) |
| Hashování | MD5-crypt → SHA-1 |
| Vyhledávání | POST `/api/search/` (XML odpověď) |
| Stream | POST `/api/file_link/` → přímý HTTPS odkaz |

## Changelog

### 1.0.0

- Počáteční vydání
- Plná podpora přihlášení, vyhledávání a streamování
