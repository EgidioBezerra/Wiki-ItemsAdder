# HUDs, GUIs...

Para ver como usar a API de HUDs e GUIs \(Font Imagens\) você pode olhar os meus exemplos:

{% embed url="https://github.com/LoneDev6/API-ItemsAdder-Example-GUI" %}

{% embed url="https://github.com/LoneDev6/API-ItemsAdder-Example-ServerMonitor" %}



### Acessar a barra de mana por exemplo

```java
PlayerHUDsHolderWrapper huds = new PlayerHUDsHolderWrapper(player);
PlayerQuantityHudWapper manaHud = 
                new PlayerQuantityHudWapper(huds, "magiccraft:mana_bar");
manaHud.setFloatValue(2.0f);
```

## FAQ

{% page-ref page="../../plugin-usage/adding-content/advanced/font-images/common-errors.md" %}

### Usar Emoji ou caracteres de GUI

```java
new FontImageWrapper("twitteremojis:confirm").getString()
```

