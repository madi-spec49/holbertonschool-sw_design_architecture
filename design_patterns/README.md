# Design Patterns en Python

## 📌 Introduction

Les **Design Patterns** (patrons de conception) sont des solutions réutilisables à des problèmes fréquents rencontrés lors du développement logiciel.

Ils permettent de :

- améliorer la maintenabilité du code
- réduire le couplage
- favoriser la réutilisation
- rendre l’architecture plus claire

Les patterns sont généralement classés en 3 catégories :

1. **Créationnels**
2. **Structurels**
3. **Comportementaux**

---

# 1. Patterns Créationnels

## Singleton

Garantit qu’une classe ne possède qu’une seule instance.

### Exemple Python

```python
class Singleton:
    _instance = None

    def __new__(cls):
        if cls._instance is None:
            cls._instance = super().__new__(cls)
        return cls._instance


a = Singleton()
b = Singleton()

print(a is b)  # True