---
title: Observer
publish: true
---

# Observer
## O que é?
No observer, você tem um objeto que irá manter o registro de todo mundo que se inscrever e, quando ocorrer a condicional de execução, você irá chamar o callback de cada um dos inscritos.

Na Unity, você pode utilizar um `public static event Action`:
```c#
public static event Action onAction;

private void OnEnable() => onAction += method_to_be_called;

private void method_to_be_called(){}

//para executar os eventos registrados:
onAction?.Invoke();

```