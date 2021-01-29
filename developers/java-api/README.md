# ☕️Java API

## Como obter a API

Você só precisa usar **maven** ou **gradle**, para obter a **API** aqui

{% embed url="https://github.com/LoneDev6/ItemsAdder-API\#-packages" %}

## Descrição

O ItemsAdder inclue uma API facil de usar para desenvolvedores Java.
Para ter acesso apenas inclua **dev.lone.itemsadder.api.ItemsAdder** em seu codigo.

## API antiga:

```java
// Garante que o ItemsAdder acabou de carregar e se que todos os seu itens estão disponiveis
// POR FAVOR USE ItemsAdderFirstLoadEvent NO LUGAR
public static boolean areItemsLoaded()

// Garante que um item customizado é feito com o ItemsAdder
public static boolean isCustomItem(ItemStack itemStack)
public static boolean isCustomItem(String customItemName)

// Obtem um item customizado do ItemsAdder a partir de seu nome na config
public static ItemStack getCustomItem(String nameInConfig)

// Spawna um bloco feito com o ItemsAdder especificando o itemstack 
// (o obtenha com getCustomItem)
public static void placeCustomBlock(Location location, ItemStack customBlock)
public static void placeCustomBlock(Location location, ItemStack customBlock, boolean lightweight)

// Obtem loot de blocos customizados
public static List<ItemStack> getCustomBlockLoot(Block block, ItemStack tool, boolean includeSelfBlock)

// Verifica sem um bloco no mundo é um blocos customizado feito com o ItemsAdder
public static boolean isCustomBlock(Block block)

// Planta uma semente customizada como uma jogador normal faria
public static void placeCustomCrop(Location location, ItemStack seed)

// Verifica se o bloco é uma planta que foi plantado com uma semente customizada
public static boolean isCustomCrop(Block block)

// Obtem uma semente de uma planta customizada
public static String getCustomSeedNameFromCrop(Block block)

// Retorna o ItemStack de um bloco customizado no mundo
public static ItemStack getCustomBlock(Block block)

// Verifica se uma entidade no mundo é um movel
public static boolean isFurniture(Entity entity)

// Verifica se o ItemStack é um item customizado especifico
// (Exemplo: verifica se a picareta é uma 'amethyst_pickaxe')
public static boolean matchCustomItemName(ItemStack itemStack, String customItemName)

// Obtem o nome do item na config (ex: 'ruby_pickaxe')
public static String getCustomItemName(ItemStack itemStack)

// Obtem o nome da config em que o item foi declarado (ex: 'items/swords')
public static String getCustomItemFileName(ItemStack itemStack)

// Obtém os usos restantes deste item (-999 se não tem uma quantidade de usos especificos = infinito)
public static int getCustomItemUsages(ItemStack itemStack)

//set custom item durability (also works with vanilla items and with
// Define a durabilidade de um item customizado (também funciona com itens padrão 
// e com itens customizados com a durabilidade padrão)
public static ItemStack setCustomItemDurability(ItemStack item, int durability)

// Obtem a durabilidade customizada
public static int getCustomItemDurability(ItemStack itemStack)

// Obtem a durabilidade customizada maxima
public static int getCustomItemMaxDurability(ItemStack itemStack)
```

