# Cvičení git merge

## Cvičení 1

1. Vypište všechny větve.
2. Postupně všechny větve slučte do hlavní větve.
3. Dostaňte tyto změny do vzdáleného repositáře.
4. Na GitHubu si zobrazte komity v hlavní větvi. Všimněte si, jak vypadá historie hlavní větve.
5. Smažte všechny sloučené větve.

### Řešení 1

```bash
git branch
git merge test-branch -m "merge 1"
git merge feature/test-branch -m "merge 2"
git merge feature/europa-file -m "merge 3"
git merge feature/bug-fix -m "merge 4"
git push
git branch -D test-branch feature/test-branch feature/europa-file feature/bug-fix   # Smazano pouze lokalne.
```

## Cvičení 2

1. Vytvořte novou větev „feature/new-moon-files“ z hlavní větve a přepněte se do ní.
2. Postupně vytvořte nový soubor s názvem Charon.txt, komitněte tuto změnu, nový soubor Měsíc.txt a komitněte.
3. Připište nový řádek „New Pluto moon“ do souboru Charon.txt a komitněte změnu.
4. Připište nový řádek „New Earth moon“ do souboru Měsíc.txt a komitněte změnu.
5. Slučte tyto změny do hlavní větve tak, aby vznik pouze jeden jediný komit v hlavní větvi.
6. Smažte větev „feature/new-moon-files“.

### Řešení 2

```bash
git switch -c feature/new-moon-files
git add ./Charon.txt
git commit -m "new Charon"
git add ./Měsíc.txt
git commit -m "new Mesic"
git commit -am "Update Charon"
git commit -am "Update Mesic"
git switch totry
git merge feature/new-moon-files -m "only one merge"
git branch -d feature/new-moon-files
```
