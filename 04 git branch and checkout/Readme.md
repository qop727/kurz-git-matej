# Cvičení git branch & git checkout

## Cvičení 1

1. Vytvořte novou větev s názvem "test-branch"
2. Přepněte se na tuto větev pomocí příkazu git checkout.
3. Vytvořte nový soubor Neptun.txt.
4. Komitněte tyto změny na této nové větvi.
5. Vraťte se zpět na hlavní větev a ověřte, že změny **nejsou** viditelné.

### Řešení 1

```bash
git checkout -b test-branch     # Nebo jde pouzit git switch -c test-branch.
git add ./Neptun.txt            # Novy soubor je nutne nejprve pridat git add.
git commit -m "new Neptun"      # U noveho souboru nejde pouzit git commit -a a prespocit tak git add.
git switch totry
git log
```

## Cvičení 2

1. Na jeden příkaz, vytvořte novou větev „feature/test-branch“ a přepněte se do ní.
2. Všimněte si, že větev se jmenuje stejně jako v předchozím příkladu. Popřemýšlejte proč.
3. Vytvořte nový soubor Pluto.txt
4. Udělejte komit.

### Řešení 2

```bash
git checkout -b feature/test-branch     # Nebo jde pouzit git switch -c feature/test-branch.
git add ./Pluto.txt                     # Novy soubor je nutne nejprve pridat git add.
git commit -m "new Pluto"               # U noveho souboru nejde pouzit git commit -a a prespocit tak git add.
```

## Cvičení 3

1. Na hlavní větvi vytvořte soubor Europa.txt.
2. Přesuňte ho do stage area.
3. Vytvořte a přepněte se do nové větve „feature/europa-file“.
4. Proveďte komit. Všimněte si, v jaké větvi soubor skončil. Pokud to není zřejmé, přepněte se mezi větvemi „feature/europa-file“ a hlavní větví.

### Řešení 3

```bash
git add ./Europa.txt
git switch -c feature/europa-file
git commit -m "new Europa"
git switch totry
git switch feature/europa-file
```

## Cvičení 4

1. Přepněte se do větve „feature/europa-file“.
2. Zkuste vytvořit novou větev s názvem „test-branch“. Všimněte si, jak bude git reagovat.

### Řešení 4

```bash
git switch feature/europa-file
git switch -c test-branch           # fatal: a branch named 'test-branch' already exists
```

## Cvičení 5

1. Vypište všechny větve ve vašem repozitáři. Povšimněte si, jak dává Git najevo, která větev je aktivní.

### Řešení 5

```bash
git branch
```

## Cvičení 6

1. Vytvořte novou větev „test-feature“.
2. Nyní tuto větev smažte.

### Řešení 6

```bash
git switch -c test-feature
git switch totry                # Je nutne prepnout se z vetve, kterou chceme smazat.
git branch -d test-feature
```
