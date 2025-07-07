# Aprende GitHub Actions

Este repositorio está diseñado para ayudarte a aprender y practicar **GitHub Actions**, la herramienta de automatización de flujos de trabajo (workflows) de GitHub.

## ¿Qué es GitHub Actions?

GitHub Actions te permite automatizar tareas como compilación, pruebas, despliegue y más, directamente desde tu repositorio. Puedes definir flujos de trabajo usando archivos YAML ubicados en `.github/workflows/`.

## Conceptos básicos

- **Workflow:** Es un proceso automatizado que se ejecuta en respuesta a eventos en tu repositorio (por ejemplo, push, pull request).
- **Job:** Un conjunto de pasos que se ejecutan en el mismo entorno.
- **Step:** Una tarea individual dentro de un job, como ejecutar un comando o una acción.
- **Action:** Una acción reutilizable que realiza una tarea específica.

## Ejemplo de condición en un workflow

Puedes controlar cuándo se ejecuta un job o step usando la instrucción `if`.  
Por ejemplo:

```yaml
if: ${{ github.ref == 'refs/heads/main' }}
```

Esto significa que el job o step solo se ejecutará si el evento ocurre en la rama principal (`main`).

### ¿Qué significa `refs/heads/main`?

- `refs` indica que es una referencia de Git.
- `heads` señala que es una rama.
- `main` es el nombre de la rama.

Por ejemplo, `refs/heads/develop` sería la rama de desarrollo.

## Recursos útiles

- [Documentación oficial de GitHub Actions](https://docs.github.com/actions)
- [Aprende sobre contextos y expresiones](https://docs.github.com/actions/learn-github-actions/contexts)

---

¡Explora los archivos de este repositorio y comienza a crear tus propios flujos de trabajo con