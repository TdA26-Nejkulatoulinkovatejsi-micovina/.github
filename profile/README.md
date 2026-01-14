# Nejkulaťoulinkovatější míčovina

Název týmu: nejkulaťoulinkovatější míčovina

## Členové a jejich role
- [Martin Petr](https://github.com/MartinGamesCZ) - Vývoj, testování
- [Lukáš Rais](https://github.com/MejPok) - Testování, v dalších fázích vývoj a komunikace s klientem
- [Filip Zima](https://github.com/ZimaJeKing) - Testování, v dalších fázích vývoj a komunikace s klientem

## Použité technologie
- Frontend: NextJS (React, TypeScript), Tailwind
- Backend: NestJS (TypeScript), TypeORM
- Ostatní: Bun runtime, TimescaleDB (pg 17 based), Traefik pro reverse proxy

## Struktura repozitářů
Pro jednodušší a přehlednější práci je aplikace rozdělena na několik menších repozitářů, kde App je hlavní repozitář obsahující další. Po push do main branch nějakého repozitáře se automaticky aktualizuje reference na něj v App repu. 

Pro klonování je tedy nutné použít tento příkaz:
```sh
git clone https://github.com/TdA26-Nejkulatoulinkovatejsi-micovina/App.git --recurse-submodules
```

## Spuštění aplikace
### Produkční režim
Stačí udělat pull request a merge v App repu: main -> production. GitHub akce se postará o zbytek. Pak už jen stačí v Tour De Cloud aplikaci nasadit a počkat.

### Vývojový režim
1. Naklonujeme si celé repo, včetně submodules:
```sh
git clone https://github.com/TdA26-Nejkulatoulinkovatejsi-micovina/App.git --recurse-submodules
```
2. V root složce naklonovaného repa (tj root složka App repa) spustíme příkaz:
```sh
docker compose -f dev.compose.yml up --build
```
3. Aplikace běží na `http://localhost:1000`

## Rychlost nasazení
Nahrání image na Tour De Cloud (action) zabere pod 5 minut, samotné nasazení přes TdC pak dalších pár minut. 
