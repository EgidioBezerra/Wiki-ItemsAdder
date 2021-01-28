# CMI

{% hint style="info" %}
## Se você estiver usando o sistema de chat do CMI, você tem que ler isso.
{% endhint %}

## Emoji

Abra config.yml do **ItemsAdder** e edite isso:

```yaml
font_images:
  chat:
    enabled: true
    replace-only-packets: true
```

## Ranks

1. Abra config.yml do **CMI** e edite isso \(Eu uso `%vault_prefix%` placeholder ao inves do **CMI** `{prefix}`\)

```yaml
GeneralFormat: '%vault_prefix% &f{displayName}&7: &r{message}'
```

2. Baixe [PlaceholderAPI](https://www.spigotmc.org/resources/placeholderapi.6245/) e o [Vault](https://github.com/MilkBowl/Vault/releases/latest)  
3. Instale os dois 
4. Execute este comando  `/papi ecloud download Vault`  
5. Execute este comando `/papi reload`

Acabou

