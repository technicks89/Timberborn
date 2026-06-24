# Resource & Production Control

## Resource Collection

| Building        | Resource     | Counter Min        | Counter Max         | Memory (Set)        | Memory (Reset)        |
| --------------- | ------------ | ------------------ | ------------------- | ------------------- | --------------------- |
| Lumberjack Flag | Log          | Log < 70%          | Log = 100%          | A: Log Min          | RST: Log Max          |
| Tapper Shack    | Pine Resin   | Pine Resin < 70%   | Pine Resin = 100%   | A: Pine Resin Min   | RST: Pine Resin Max   |
| Gather Flag     | Mangrove     | Mangrove < 70%     | Mangrove = 100%     | A: Mangrove Min     | RST: Mangrove Max     |
| Gather Flag     | Coffee Beans | Coffee Beans < 70% | Coffee Beans = 100% | A: Coffee Beans Min | RST: Coffee Beans Max |
| Gather Flag     | Berries      | Berries < 70%      | Berries = 100%      | A: Berries Min      | RST: Berries Max      |
| Farm House      | Kohlrabi     | Kohlrabi < 70%     | Kohlrabi = 100%     | A: Kohlrabi Min     | RST: Kohlrabi Max     |
| Farm House      | Cassava      | Cassava < 70%      | Cassava = 100%      | A: Cassava Min      | RST: Cassava Max      |
| Farm House      | Soybean      | Soybean < 70%      | Soybean = 100%      | A: Soybean Min      | RST: Soybean Max      |
| Farm House      | Canola       | Canola < 70%       | Canola = 100%       | A: Canola Min       | RST: Canola Max       |
| Farm House      | Corn         | Corn < 70%         | Corn = 100%         | A: Corn Min         | RST: Corn Max         |
| Farm House      | Eggplant     | Eggplant < 70%     | Eggplant = 100%     | A: Eggplant Min     | RST: Eggplant Max     |

## Water & Raw Materials

| Building          | Resource | Counter Min    | Counter Max     | Memory (Set)    | Memory (Reset)    | Conditions                  |
| ----------------- | -------- | -------------- | --------------- | --------------- | ----------------- | --------------------------- |
| Water Pump        | Water    | Water < 70%    | Water = 100%    | A: Water Min    | RST: Water Max    | Water Reset, Temperate      |
| Badwater Pump     | Badwater | Badwater < 70% | Badwater = 100% | A: Badwater Min | RST: Badwater Max | Badwater Reset, Not Drought |
| Hydroponic Garden | Algae    | Algae < 70%    | Algae = 100%    | A: Algae Min    | RST: Algae Max    | Water > 40%                 |
| Hydroponic Garden | Mushroom | Mushroom < 70% | Mushroom = 100% | A: Mushroom Min | RST: Mushroom Max | Water > 40%                 |
| Dirt Excavator    | Dirt     | Dirt < 70%     | Dirt = 100%     | A: Dirt Min     | RST: Dirt Max     | Power Supply > 0            |

## Intermediate Production

| Building      | Resource           | Inputs                        | Power Required |
| ------------- | ------------------ | ----------------------------- | -------------- |
| Fermenter     | Fermented Cassava  | Cassava > 10%                 | Yes            |
| Fermenter     | Fermented Mushroom | Mushroom > 10%                | Yes            |
| Oil Press     | Canola Oil         | Canola > 10%                  | Yes            |
| Lumber Mill   | Plank              | Log > 10%                     | Yes            |
| Gear Workshop | Gear               | Plank > 10%                   | Yes            |
| Metalsmith    | Metal Parts        | Scrap Metal > 10%, Log > 10%  | No             |
| Smelter       | Metal              | Scrap Metal > 10%, Log > 10%  | Yes            |
| Centrifuge    | Extract            | Badwater > 10%, Log > 10%     | Yes            |
| Wood Workshop | Treated Plank      | Plank > 10%, Pine Resin > 10% | Yes            |

## Food Production

| Building       | Resource          | Inputs                                          | Power Required |
| -------------- | ----------------- | ----------------------------------------------- | -------------- |
| Food Factory   | Corn Rations      | Corn > 10%                                      | Yes            |
| Food Factory   | Algae Rations     | Algae > 10%, Canola Oil > 10%                   | Yes            |
| Food Factory   | Eggplant Rations  | Eggplant > 10%, Canola Oil > 10%                | Yes            |
| Fermenter      | Fermented Soybean | Soybean > 10%, Canola Oil > 10%                 | Yes            |
| Coffee Brewery | Coffee            | Coffee Beans > 10%, Canola Oil > 10%, Log > 10% | Yes            |

## Industry & Manufacturing

| Building            | Resource    | Inputs                          | Power Required |
| ------------------- | ----------- | ------------------------------- | -------------- |
| Scavenger Flag/Mine | Scrap Metal | Treated Plank > 10%             | Yes            |
| Explosives Factory  | Explosive   | Badwater > 10%                  | Yes            |
| Explosives Factory  | Firework    | Badwater > 10%                  | Yes            |
| Grease Factory      | Grease      | Extract > 10%, Canola Oil > 10% | Yes            |

## Bot Production

| Building         | Resource   | Inputs                               | Power Required |
| ---------------- | ---------- | ------------------------------------ | -------------- |
| Bot Part Factory | Bot Limbs  | Plank > 10%, Gear > 10%              | Yes            |
| Bot Part Factory | Bot Chasis | Plank > 10%, Metal > 10%             | Yes            |
| Bot Part Factory | Bot Heads  | Plank > 10%, Gear > 10%, Metal > 10% | Yes            |

## Power Generation

| Building     | Input 1     | Input 2   | Condition   |
| ------------ | ----------- | --------- | ----------- |
| Steam Engine | Water > 40% | Log > 10% | Surplus < 0 |

## Science Control

| Building        | Science Min    | Science Max      | Set            | Reset            | Condition   |
| --------------- | -------------- | ---------------- | -------------- | ---------------- | ----------- |
| Number Cruncher | Science < 5000 | Science > 100000 | A: Science Min | RST: Science Max | Surplus < 0 |

## Control Tower

| Building      | Requirement  | Power            |
| ------------- | ------------ | ---------------- |
| Control Tower | Science > 20 | Power Supply > 0 |

## Population Control

| Building          | Population Min          | Population Max          | Inputs                                             | Power            |
| ----------------- | ----------------------- | ----------------------- | -------------------------------------------------- | ---------------- |
| Contamination Pod | Contaminated Beaver = 1 | Contaminated Beaver > 0 | Extract > 10%                                      | Power Supply > 0 |
| Bot               | Unemployed Bot < 10     | Unemployed Bot = 20     | Bot Limbs > 20%, Bot Heads > 10%, Bot Chasis > 10% | Power Supply > 0 |
|                   |                         |                         |                                                    |                  |
