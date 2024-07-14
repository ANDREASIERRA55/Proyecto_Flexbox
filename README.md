# Proyecto_Flexbox
# Crear .gitignore si no existe y añadir .DS_Store
touch .gitignore
echo ".DS_Store" >> .gitignore

# Despreparar .DS_Store y eliminarlo del control de versiones
git restore --staged .DS_Store
git rm --cached .DS_Store

# Hacer commit y push de los cambios en .gitignore
git add .gitignore
git commit -m "Añadir .DS_Store al .gitignore"
git push origin main

# Traer cambios del repositorio remoto
git fetch origin

# Restaurar el archivo .gitignore desde el remoto
git checkout origin/main -- .gitignore

# Añadir y hacer commit del archivo restaurado
git add .gitignore
git commit -m "Recuperar archivo .gitignore"
git push origin main
