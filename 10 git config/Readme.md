# Cvičení git nastaveni

## Cvičení 1

1. Nastavte si své jméno a e-mail pro komitování.
2. Zobrazte nastavení pro váš lokální repozitář.
3. Nastavte si své nové jméno (prohoďte třeba pořadí jména a příjmení) a email pro komitování pouze pro jeden konkrétní repozitář.
4. Vytvořte si novou větev „new-collaborator“.
5. Přidejte nový soubor Titan.txt
6. Komitněte změny.
7. Zobrazte historii komitů a zkontrolujte si, že komit je podepsaný opravdu novým jménem.

### Řešení 1

```bash
git config --global user.name "Matěj H"
git config --global user.email "qop727@gmail.com"
git config --local --list
git config --local user.name "H Matěj"
git config --local user.email "qop727@gmail.com"
git switch -c new-collaborator
git add ./Titan.txt
git commit -m "new Titan"
git log -- Titan.txt
```
