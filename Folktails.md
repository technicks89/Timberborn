# 🏭 Folktails Automation Logic Sheet

## 🌲 Raw Resource Production

| Building | Resource | Resource Counter Min | Resource Counter Max | Memory : Set-Reset | Memory : Set-Reset  | Power Meter | Relay: AND | Relay: AND |
|----------|----------|----------------------|----------------------|---------------------|---------------------|-------------|--------|--------|
| Scavenger Flag | Scrap Metal | Scrap Metal < 70% | Scrap Metal = 100% | A: Scrap Metal Min | RST: Scrap Metal Max |
| Lumberjack Flag | Log | Log < 70% | Log = 100% | A: Log Min | RST: Log Max |
| Tapper Shack | Pine Resin | Pine Resin < 70% | Pine Resin = 100% | A: Pine Resin Min | RST: Pine Resin Max |
| Tapper Shack | Maple Syrup | Maple Syrup < 70% | Maple Syrup = 100% | A: Maple Syrup Min | RST: Maple Syrup Max |
| Gather Flag | Chestnut | Chestnut < 70% | Chestnut = 100% | A: Chestnut Min | RST: Chestnut Max |
| Gather Flag | Dandelion | Dandelion < 70% | Dandelion = 100% | A: Dandelion Min | RST: Dandelion Max |
| Gather Flag | Berries | Berries < 70% | Berries = 100% | A: Berries Min | RST: Berries Max |
| Farm House | Sunflower | Sunflower < 70% | Sunflower = 100% | A: Sunflower Min | RST: Sunflower Max |
| Farm House | Carrot | Carrot < 70% | Carrot = 100% | A: Carrot Min | RST: Carrot Max |
| Farm House | Potato | Potato < 70% | Potato = 100% | A: Potato Min | RST: Potato Max |
| Farm House | Wheat | Wheat < 70% | Wheat = 100% | A: Wheat Min | RST: Wheat Max |
| Aquatic Farm House | Cattail Root | Cattail Root < 70% | Cattail Root = 100% | A: Cattail Root Min | RST: Cattail Root Max |
| Aquatic Farm House | Spadderdock | Spadderdock < 70% | Spadderdock = 100% | A: Spadderdock Min | RST: Spadderdock Max |
| (Large) Water Pump | Water | Water < 70% | Water = 100% | A: Water Min | RST: Water Max |  | Water Reset | Temperate |
| Badwater Pump | Badwater | Badwater < 70% | Badwater = 100% | A: Badwater Min | RST: Badwater Max |  | Badwater Reset | Not Drought |
| Dirt Excavator | Dirt | Dirt < 70% | Dirt = 100% | A: Dirt Min | RST: Dirt Max | Power Supply > 0 | Dirt Reset | Power |

## 🪵 Processing & Refining

| Building | Resource | Resource Counter Min | Resource Counter Max | Memory : Set-Reset | Memory : Set-Reset | Resource Counter Empty 1 | Resource Counter Empty 2 | Power Meter | Relay: AND | Relay: AND | Relay: AND |
|----------|----------|----------------------|----------------------|---------------------|---------------------|---------------------------|---------------------------|-------------|--------|--------|--------|
| Mine | Scrap Metal | Scrap Metal < 70% | Scrap Metal = 100% | A: Scrap Metal Min | RST: Scrap Metal Max | Treated Plank > 10% |  | Power Supply > 0 | Scrap Metal Reset | Treated Plank Empty | Power |
| Lumber Mill | Plank | Plank < 70% | Plank = 100% | A: Plank Min | RST: Plank Max | Log > 10% |  | Power Supply > 0 | Plank Reset | Log Empty | Power |
| Gear Workshop | Gear | Gear < 70% | Gear = 100% | A: Gear Min | RST: Gear Max | Plank > 10% |  | Power Supply > 0 | Gear Reset | Plank Empty | Power |
| Paper Mill | Paper | Paper < 70% | Paper = 100% | A: Paper Min | RST: Paper Max | Log > 10% |  | Power Supply > 0 | Paper Reset | Log Empty | Power |
| Printing Press | Book | Book < 70% | Book = 100% | A: Book Min | RST: Book Max | Paper > 10% |  | Power Supply > 0 | Book Reset | Paper Empty | Power |
| Explosives Factory | Explosive | Explosive < 70% | Explosive = 100% | A: Explosive Min | RST: Explosive Max | Badwater > 10% |  | Power Supply > 0 | Explosive Reset | Badwater Empty | Power |
| Explosives Factory | Firework | Firework < 70% | Firework = 100% | A: Firework Min | RST: Firework Max | Badwater > 10% |  | Power Supply > 0 | Firework Reset | Badwater Empty | Power |
| Gristmill | Wheat Flour | Wheat Flour < 70% | Wheat Flour = 100% | A: Wheat Flour Min | RST: Wheat Flour Max | Wheat > 10% |  | Power Supply > 0 | Wheat Flour Reset | Wheat Empty | Power |
| Gristmill | Cattail Flour | Cattail Flour < 70% | Cattail Flour = 100% | A: Cattail Flour Min | RST: Cattail Flour Max | Cattail Root > 10% |  | Power Supply > 0 | Cattail Flour Reset | Cattail Empty | Power |

## 🍳 Food Production

| Building | Resource | Resource Counter Min | Resource Counter Max | Memory : Set-Reset | Memory : Set-Reset | Resource Counter Empty 1 | Resource Counter Empty 2 | Resource Counter Empty 3 | Power Meter | Relay: AND | Relay: AND | Relay: AND | Relay: AND |
|----------|----------|----------------------|----------------------|---------------------|---------------------|---------------------------|---------------------------|---------------------------|-------------|--------|--------|--------|--------|
| Grill | Grilled Potato | Grilled Potato < 70% | Grilled Potato = 100% | A: Grilled Potato Min | RST: Grilled Potato Max | Potato > 10% | Log > 10% |  |  | Grilled Potato Reset | Potato Empty | Log Empty |
| Grill | Grilled Chestnut | Grilled Chestnut < 70% | Grilled Chestnut = 100% | A: Grilled Chestnut Min | RST: Grilled Chestnut Max | Chestnut > 10% | Log > 10% |  |  | Grilled Chestnut Reset | Chestnut Empty | Log Empty |
| Grill | Grilled Spadderdock | Grilled Spadderdock < 70% | Grilled Spadderdock = 100% | A: Grilled Spadderdock Min | RST: Grilled Spadderdock Max | Spadderdock > 10% | Log > 10% |  |  | Grilled Spadderdock Reset | Spadderdock Empty | Log Empty |
| Bakery | Bread | Bread < 70% | Bread = 100% | A: Bread Min | RST: Bread Max | Wheat Flour > 10% | Log > 10% |  |  | Bread Reset | Wheat Flour Empty | Log Empty |
| Bakery | Cattail Cracker | Cattail Cracker < 70% | Cattail Cracker = 100% | A: Cattail Cracker Min | RST: Cattail Cracker Max | Cattail Flour > 10% | Log > 10% |  |  | Cattail Cracker Reset | Cattail Flour Empty | Log Empty |
| Refinery | Biofuel | Biofuel < 70% | Biofuel = 100% | A: Biofuel Min | RST: Biofuel Max | Potato/Carrot/Spadderdock > 10% | Water > 10% |  |  | Biofuel Reset | Potato/Carrot/Spadderdock Empty | Water Empty |
| Refinery | Catalyst | Catalyst < 70% | Catalyst = 100% | A: Catalyst Min | RST: Catalyst Max | Maple Syrup > 10% | Extract > 10% |  |  | Catalyst Reset | Maple Syrup Empty | Extract Empty |
| Bakery | Maple Pastry | Maple Pastry < 70% | Maple Pastry = 100% | A: Maple Pastry Min | RST: Maple Pastry Max | Wheat Flour > 10% | Maple Syrup > 10% | Log > 10% | Power Supply > 0 | Maple Pastry Reset | Wheat Flour Empty | Maple Syrup Empty | Power |
| Herbalist | Antidote | Antidote < 70% | Antidote = 100% | A: Antidote | RST: Anitdote | Paper > 10% | Dandelion > 10% | Berries > 10% |  | Antidote Reset | Paper Empty | Dandelion Empty | Berries Empty |

## 🔩 Advanced Manufacturing

| Building | Resource | Resource Counter Min | Resource Counter Max | Memory : Set-Reset | Memory : Set-Reset | Resource Counter Empty 1 | Resource Counter Empty 2 | Resource Counter Empty 3 | Power Meter | Relay: AND | Relay: AND | Relay: AND | Relay: AND | Relay: AND |
|----------|----------|----------------------|----------------------|---------------------|---------------------|---------------------------|---------------------------|---------------------------|-------------|--------|--------|--------|--------|--------|
| Wood Workshop | Treated Plank | Treated Plank < 70% | Treated Plank = 100% | A: Treated Plank Min | RST: Treated Plank Max | Plank > 10% | Pine Resin > 10% |  | Power Supply > 0 | Treated Plank Reset | Plank Empty | Pine Resin Empty | Power |  |
| Smelter | Metal | Metal < 70% | Metal = 100% | A: Metal Min | RST: Metal Max | Scrap Metal > 10% | Log > 10% |  | Power Supply > 0 | Metal Reset | Scrap Metal Empty | Log Empty | Power |  |
| Centrifuge | Extract | Extract < 70% | Extract = 100% | A: Extract Min | RST: Extract Max | Badwater > 10% | Log > 10% | Power Supply > 0 | Extract Reset | Badwater Empty | Log Empty | Power |
| Printing Press | Punch Card | Punch Card < 70% | Punch Card = 100% | A: Punch Card Min | RST: Punch Card Max | Paper > 10% | Plank > 10% |  | Power Supply > 0 | Punch Card Reset | Paper Empty | Plank Empty | Power |  |
| Bot Part Factory | Bot Limbs | Bot Limbs < 70% | Bot Limbs = 100% | A: Bot Limbs Min | RST: Bot Limbs Max | Plank > 10% | Gear > 10% |  | Power Supply > 0 | Bot Limbs Reset | Plank Empty | Gear Empty | Power |  |
| Bot Part Factory | Bot Heads | Bot Heads < 70% | Bot Heads = 100% | A: Bot Heads Min | RST: Bot Heads Max | Plank > 10% | Gear > 10% | Metal > 10% | Power Supply > 0 | Bot Heads Reset | Plank Empty | Gear Empty | Metal Empty | Power |
| Bot Part Factory | Bot Chassis | Bot Chassis < 70% | Bot Chassis = 100% | A: Bot Chassis Min | RST: Bot Chassis Max | Plank > 10% | Metal > 10% | Biofuel > 10% | Power Supply > 0 | Bot Chassis Reset | Plank Empty | Metal Empty | Biofuel Empty | Power |

## 👥 Population Control Systems

| Building | Population Counter Min | Population Counter Max | Memory : Set-Reset | Memory : Set-Reset | Power Meter | Relay: AND | Relay: AND |
|----------|------------------------|------------------------|---------------------|---------------------|-------------|--------|--------|
| Observatory | Unemployed = 0 | Unemployed > 4 | A: Unemployed Max | RST: Unemployed Min | Surplus > 0 | Unemployed Reset | Power |

## 🤖 Bot Workforce Tracking

| Resource | Population Counter Min | Population Counter Max | Memory : Set-Reset | Memory : Set-Reset | Resource Counter Empty 1 | Resource Counter Empty 2 | Resource Counter Empty 3 | Power Meter | Relay: AND | Relay: AND | Relay: AND | Relay: AND | Relay: AND |
|----------|------------------------|------------------------|---------------------|---------------------|---------------------------|---------------------------|---------------------------|-------------|--------|--------|--------|--------|--------|
| Bot | Unemployed Bot < 10 | Unemployed Bot = 20 | A: Unemployed Bot Min | RST: Unemployed Bot Max | Bot Limbs > 20% | Bot Heads > 10% | Bot Chassis > 10% | Power Supply > 0 | Unemployed Bot Reset | Bot Limbs Empty | Bot Heads Empty | Bot Chassis Empty | Power |
