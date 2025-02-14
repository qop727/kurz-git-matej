# Cvičení git push

## Cvičení 1

1. Nahrajte své změny z cvičení git branch & git checkout do vzdáleného repozitáře na GitHubu.
2. Zkontrolujte, že na webu vidíte všechny větve.

### Řešení 1

```bash
git push
```

## Cvičení 2

1. Přepněte se na hlavní větev.
2. Vytvořte novou větev s názvem „feature/bug-fix“.
3. Upravte soubor Jupiter.txt a připište do něj řádek „Bug fix Jupiter file“.
4. Dostaňte tuto změnu do vzdáleného repozitáře na GitHubu.

### Řešení 2

```bash
git switch totry
git switch -c feature/bug-fix
git commit -am "Big fix Jupiter"
git push -u origin feature/bug-fix
```

## Cvičení 3

1. Na hlavní větvi změňte skrze webové rozhraní GitHubu soubor Země.txt. Připište nový řádek „Update Earth file“.
2. Proveďte komit změny.
3. Na hlavní větvi v lokálním repozitáři, upravte soubor Uran.txt a připište do něj nový řádek „Update Uran file“.
4. Proveďte komit této změny.
5. Nyní tuto změnu dostaňte na vzdálený repozitář na GitHubu.

### Řešení 3

```bash
git commit -am "Update Uran"
git pull --rebase origin totry      # Nebo lze pouzit git pull origin totry.
git push
```
