---
description: ItemsAdder é compativel com MMOItems e é de facil integração.
---

# MMOItems

Baixe **MMOItems** [aqui](https://www.spigotmc.org/resources/mmoitems-premium.39267/)

## Aqui você pode baixar o pacote de exemplo mostrado nesse tutorial

{% embed url="https://www.spigotmc.org/resources/items-mmoitem-example-integration.88351/" %}

## Como conectar um MMOItem a um item customizado do ItemsAdder

{% hint style="warning" %}
ATUALIZE O **ITEMSADDER** PARA A VERSÃO **2.1.29+** E O **MMOITEM** PARA A VERSÃO **6.5.1+**
{% endhint %}

### - Use o comando /mmoitems browse

![](../../.gitbook/assets/immagine%20%2829%29.png)

### - Crie um novo MMOItem

![](../../.gitbook/assets/immagine%20%2835%29.png)

![](../../.gitbook/assets/immagine%20%2836%29.png)

### - Adicione todos os atributos que você quiser, por exemplo dano magico, etc

![](../../.gitbook/assets/immagine%20%2828%29.png)

### - Verifique o MMOItem criado dentro do /mmoitems browse

![](../../.gitbook/assets/immagine%20%2838%29.png)

## Crie um item do ItemsAdder

### - Crie o seu arquivo .yml normalmente e adicione todas as propriedades do item do ItemsAdder

![](../../.gitbook/assets/immagine%20%2830%29.png)

{% hint style="success" %}
Como você pode ver eu coloquei um novo atributo chamado **`mmoitem`** tambem **`type`** e **`id`**.
Eles são usados para **conectar** os **dois items**.
{% endhint %}

```yaml
info:
  namespace: mmoitems_example
items:
  test:
    display_name: ""
    permission: example_item
    mmoitem:
      type: SWORD
      id: TEST
    resource:
      material: DIAMOND_SWORD
      generate: true
      textures:
      - item/test.png
    durability:
      max_custom_durability: 1324
```

### - Crie a sua textura .png normalmente

![](../../.gitbook/assets/immagine%20%2832%29.png)

### - Pegue o item

Use o comando `/iaget mmoitems_example:example_item` para pegar o seu item finalizado

![](../../.gitbook/assets/immagine%20%2833%29.png)

![](../../.gitbook/assets/immagine%20%2837%29.png)

