# Cvičení git commit

> Pracujte se svým veřejným repozitářem.

## Cvičení 1

1. Použijte změny z cvičení git add. (_nekopírujte kód z řešení, pouze prostě pokračujte_)
2. Vytvořte nový komit s komentářem "Initial commit".
3. Ověřte pomocí příkazu git log, že se komit úspěšně vytvořil.

### Řešení 1

```bash
git commit -m "Initial commit"
git log
```

## Cvičení 2

1. Vytvořte nový soubor Uran.txt.
2. Vytvořte nový komit s komentářem "Add Uran".
3. Ověřte pomocí příkazu git log, že se komit úspěšně vytvořil.

### Řešení 2

```bash
git add ./Uran.txt
git commit -m "Add Uran"
git log
```

## Cvičení 3

1. Upravte soubor Merkur.txt vepište do něj text „Hello world“.
2. Vytvořte nový komit s komentářem "Update first test".
3. Ověřte pomocí příkazu git log, že se komit úspěšně vytvořil.

### Řešení 3

```bash
git add ./Merkur.txt
git commit -m "Update first test"
git log
```

## Cvičení 4

1. Upravte soubory Venuše.txt, Země.txt, Mars.txt a do každého z nich vepište název samotného souboru, tj. „Venuše.txt“ do souboru Venuše.txt, „Země.txt“ do Země.txt atd.
2. Vytvořte nový komit s komentářem "Update integration tests" a zahrňte všechny změny najednou, tak abyste vše udělali na 1 příkaz Gitu.
3. Ověřte pomocí příkazu git log, že se komit úspěšně vytvořil.

### Řešení 4

```bash
git commit -am "Update integration tests"
git log
```

## Cvičení 5

1. Přepište soubor Uran.txt s novým prázdným souborem (_nebo kompletně vymažte jeho obsah_).
2. Vytvořte nový komit, který přidá tento soubor do repozitáře a bude mít komentář „Add Uran“.
3. Upravte existující komit a změňte jeho komentář, aby byl „Clear Uran file“.

### Řešení 5

```bash
git commit -am "Add Uran"
git commit -a --amend --only -m "Clear Uran file"
```
