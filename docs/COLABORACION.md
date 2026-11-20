# Colaboración GitHub + Kiro

## Organización
- Propietario: `LeonardoSolis0303`.
- Integrante frontend: rama `frontend`, modifica principalmente `dashboard/`.
- Integrante backend: rama `backend`, modifica principalmente `backend/`.
- `main` reúne cambios revisados mediante pull requests.
- Cada integrante utiliza su Kiro IDE y su clon local; no es una sesión de agente compartida.

## Primera instalación
Clona el repositorio en una carpeta **nueva**, sin reemplazar una demo anterior.

```bash
git clone https://github.com/LeonardoSolis0303/nfl-data-hack-unam-1.git
cd nfl-data-hack-unam-1
```

Frontend (Arch Linux u otro sistema):
```bash
git switch --track origin/frontend
```

Backend (Windows PowerShell o cualquier sistema):
```powershell
git switch --track origin/backend
```

Si una rama local ya existe, cambia con `git switch frontend` o `git switch backend`.

## Ciclo de trabajo
1. Verifica `git status` y la rama activa.
2. Edita solo tu área asignada.
3. Ejecuta las pruebas que existan; no simules resultados.
4. Ejecuta `git add <archivos>`, `git commit -m "..." ` y `git push -u origin <rama>`.
5. En GitHub abre un pull request de tu rama hacia `main`.
6. Revisa conflictos y evidencia antes de integrar. Sin `push --force`.

## Actualizarse tras integrar a main
Desde una rama limpia, trae primero las actualizaciones:
```bash
git fetch origin
```
Consulta los cambios antes de mezclar `main` con tu rama. En caso de conflicto, resuélvelo entre los dos; no sobrescribas unilateralmente trabajo ajeno.

## Integrar demos existentes
Si algún integrante tiene una demo en `C:\demoNFL` u otra carpeta, **no clones encima de ella**. Clona en un lugar nuevo y copia manualmente únicamente los archivos útiles a la rama correspondiente, después de revisar sus dependencias y procedencia.

## Aprobaciones y permisos
Para trabajar en un repositorio público basta el acceso de lectura para clonar, pero se requiere permiso de escritura para publicar ramas. El propietario debe invitar al colaborador en GitHub si aún no tiene acceso. La invitación se acepta desde la cuenta del colaborador.

La creación de esta estructura no significa que el frontend, la API o sus cálculos estén implementados.
