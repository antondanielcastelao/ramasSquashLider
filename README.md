# Merge con squash

## Commits iniciales

# Parte del lider
```bash
# Creamos la rama en la que vamos a trabajar
git checkout -b lider
# hacer un commit
git add .\README.md
git commit -m "A"
# hacer un commit
git add .\README.md
git commit -m "B"
# ultimo commit
git add .\README.md
git commit -m "C"
```

## Comandos colaborador
```bash
# Crea la rama de colaborador
git checkout -b colaborador
# commit a 
git commit -m "A"
# commit B
git commit -m "B"
# commit C
git commit -m "C"
```
# Merge rama colaborador
```bash
git checkout master
git merge colaborador
git add .\README.md
git commit -m "Merge listo"
```

# Hacer el merge con la rama líder
```bash
# vamos a la rama main
git checkout main
# cargamos los cambios del colaborador
git pull
# hacemos el merge squash con la rama lider
git merge --squash lider
# solo faltará corregir los conflictos y ya
```
