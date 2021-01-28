# EpicBackpacks

Baixe o plugin de mochilas [aqui](https://www.spigotmc.org/resources/%E2%9C%85must-have%E2%9C%85-epic-backpacks.28981/)

{% hint style="success" %}
Para criar mochilas que usam texturas do ItemsAdder você precisa abrir backpacks.yml \(na pasta do EpicBackpacks\) e adicione isso \(um para cada mochila que você quiser criar\):
{% endhint %}

```yaml
 cool_backpack:
    display_name: '&fCool Backpack'
    item:
      type: ITEMSADDER_ITEM
      name: "itemsadder:plastic_bag"
    size: 3
    craft_recipe:
      pattern:
        - XXX
        - LCL
        - XLX
      ingredients:
        L: LEATHER
        C: CHEST
```

