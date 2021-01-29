# Usuarios experientes

## Instalando as dependencias necessárias

* Instalar [skript](https://github.com/SkriptLang/Skript/releases)
* Instalar [skript-mirror](https://skripttools.net/addons?q=mirror)

{% hint style="info" %}
Para obter mais informações do **skript-mirror** por favor leia a [wiki](https://skript-mirror.gitbook.io/docs/)
{% endhint %}

{% hint style="danger" %}
### Por favor **não peça** por **suporte** para problemas ou questões relacionadas com **skript**.

Eu não sou um expert do skript e eu não sou o desenvolvedor do **skript** ou do **skript-mirror**.
**Qualquer questão sobre o skript será ignorada**, espero que entenda.
{% endhint %}

## Exemplos

{% tabs %}
{% tab title="Obtem um item por comando" %}
```yaml
import:
  dev.lone.itemsadder.api.ItemsAdder

command /iaskript:
  trigger:
    set {testItem} to ItemsAdder.getCustomItem("itemsadder:ruby")
    sender.getInventory().addItem({testItem})
```
{% endtab %}

{% tab title="Verifica se o bloco clicado é um bloco customizado" %}
```yaml
import:
  dev.lone.itemsadder.api.ItemsAdder
  org.bukkit.event.player.PlayerInteractEvent
  org.bukkit.inventory.EquipmentSlot as EquipmentSlot

on PlayerInteractEvent:
    if event.getHand() is EquipmentSlot.OFF_HAND: 
        stop

    set {clickedBlock} to event.getClickedBlock()
    set {isCustomBlock} to ItemsAdder.isCustomBlock({clickedBlock})
    event.getPlayer().sendMessage("Is custom block: %{isCustomBlock}%")

    if {isCustomBlock} is true:
        set {tmp} to ItemsAdder.getCustomBlock({clickedBlock})
        set {name} to {tmp}.getItemMeta().getDisplayName()
        event.getPlayer().sendMessage("%{name}%")
```
{% endtab %}

{% tab title="GUI customizada" %}
```yaml
import:
  dev.lone.itemsadder.api.ItemsAdder
  dev.lone.itemsadder.api.FontImages.TexturedInventoryWrapper
  dev.lone.itemsadder.api.FontImages.FontImageWrapper
  org.bukkit.entity.Player
  
  
		
command /iaguitest:
	trigger:
	
		set {customTexture} to new FontImageWrapper("mcguis:blank_menu")
		set {gui} to new TexturedInventoryWrapper(null, 54, "&0Test" and {customTexture})
		set {icon} to ItemsAdder.getCustomItem("mcicons:icon_confirm")
		add player to {players::*}
		set slot 12 of {gui}.getInternal() to {icon}
		{gui}.showInventory(player)
 
on inventory click:
	if {players::*} contain player:
		if index of event-slot = 12:
			cancel event
			send "Confirmed!"

on inventory close:
	remove player from {players::*}
```
{% endtab %}
{% endtabs %}



