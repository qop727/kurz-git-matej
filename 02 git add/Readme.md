# Cvičení git add

> Pracujte se svým veřejným repozitářem.

## Cvičení 1

1. Vytvořte nový soubor Merkur.txt v projektu.
2. Použijte příkaz git add na přidání souboru do stage area.
3. Ověřte pomocí příkazu git status, že se soubor úspěšně přidal.

### Řešení 1

```bash
git add ./Merkur.txt
git status
```

## Cvičení 2

1. Vytvořte 3 nové soubory Venuše.txt, Země.txt, Mars.txt v projektu.
2. Přidejte změny provedené ve všech souborech do indexu naráz.

### Řešení 2

```bash
git add .
```

## Cvičení 3

1. Vytvořte 2 nové soubory Jupiter.txt, Saturn.txt v projektu.
2. Přidejte změny provedené pouze v souboru Jupiter.txt do indexu.
3. Smažte soubor Saturn.txt a podívejte se, co na to git.

### Řešení 3

```bash
git add ./Jupiter.txt
git status
```
