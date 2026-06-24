# Production & Resource Control Table

## Resource Buildings

| Building        | Resource     | Resource Counter Min | Resource Counter Max | Memory (Set-Reset)                          | Empty 1 | Empty 2 | Empty 3 | Power Meter | Relay (AND) | Extra |
| --------------- | ------------ | -------------------- | -------------------- | ------------------------------------------- | ------- | ------- | ------- | ----------- | ----------- | ----- |
| Lumberjack Flag | Log          | Log < 70%            | Log = 100%           | A: Log Min / RST: Log Max                   |         |         |         |             |             |       |
| Tapper Shack    | Pine Resin   | Pine Resin < 70%     | Pine Resin = 100%    | A: Pine Resin Min / RST: Pine Resin Max     |         |         |         |             |             |       |
| Gather Flag     | Mangrove     | Mangrove < 70%       | Mangrove = 100%      | A: Mangrove Min / RST: Mangrove Max         |         |         |         |             |             |       |
| Gather Flag     | Coffee Beans | Coffee Beans < 70%   | Coffee Beans = 100%  | A: Coffee Beans Min / RST: Coffee Beans Max |         |         |         |             |             |       |
| Gather Flag     | Berries      | Berries < 70%        | Berries = 100%       | A: Berries Min / RST: Berries Max           |         |         |         |             |             |       |
| Farm House      | Kohlrabi     | Kohlrabi < 70%       | Kohlrabi = 100%      | A: Kohlrabi Min / RST: Kohlrabi Max         |         |         |         |             |             |       |
| Farm House      | Cassava      | Cassava < 70%        | Cassava = 100%       | A: Cassava Min / RST: Cassava Max           |         |         |         |             |             |       |
| Farm House      | Soybean      | Soybean < 70%        | Soybean = 100%       | A: Soybean Min / RST: Soybean Max           |         |         |         |             |             |       |
| Farm House      | Canola       | Canola < 70%         | Canola = 100%        | A: Canola Min / RST: Canola Max             |         |         |         |             |             |       |
| Farm House      | Corn         | Corn < 70%           | Corn = 100%          | A: Corn Min / RST: Corn Max                 |         |         |         |             |             |       |
| Farm House      | Eggplant     | Eggplant < 70%       | Eggplant = 100%      | A: Eggplant Min / RST: Eggplant Max         |         |         |         |             |             |       |

### Water & Pumping

| Building          | Resource | Min            | Max             | Memory (Set-Reset)                  | Empty 1     | Empty 2 | Empty 3 | Power Meter      | Relay (AND)    | Extra       |
| ----------------- | -------- | -------------- | --------------- | ----------------------------------- | ----------- | ------- | ------- | ---------------- | -------------- | ----------- |
| Water Pump        | Water    | Water < 70%    | Water = 100%    | A: Water Min / RST: Water Max       |             |         |         |                  | Water Reset    | Temperate   |
| Badwater Pump     | Badwater | Badwater < 70% | Badwater = 100% | A: Badwater Min / RST: Badwater Max |             |         |         |                  | Badwater Reset | Not Drought |
| Hydroponic Garden | Algae    | Algae < 70%    | Algae = 100%    | A: Algae Min / RST: Algae Max       | Water > 40% |         |         |                  | Algae Reset    | Water Empty |
| Hydroponic Garden | Mushroom | Mushroom < 70% | Mushroom = 100% | A: Mushroom Min / RST: Mushroom Max | Water > 40% |         |         |                  | Mushroom Reset | Water Empty |
| Dirt Excavator    | Dirt     | Dirt < 70%     | Dirt = 100%     | A: Dirt Min / RST: Dirt Max         |             |         |         | Power Supply > 0 | Dirt Reset     | Power       |

### Manufacturing Chains

| Building            | Resource           | Min                      | Max                       | Memory (Set-Reset)                                      | Empty 1             | Empty 2   | Empty 3 | Power Meter      | Relay (AND)              | Extra                         |
| ------------------- | ------------------ | ------------------------ | ------------------------- | ------------------------------------------------------- | ------------------- | --------- | ------- | ---------------- | ------------------------ | ----------------------------- |
| Fermenter           | Fermented Cassava  | Fermented Cassava < 70%  | Fermented Cassava = 100%  | A: Fermented Cassava Min / RST: Fermented Cassava Max   | Cassava > 10%       |           |         | Power Supply > 0 | Fermented Cassava Reset  | Cassava Empty / Power         |
| Fermenter           | Fermented Mushroom | Fermented Mushroom < 70% | Fermented Mushroom = 100% | A: Fermented Mushroom Min / RST: Fermented Mushroom Max | Mushroom > 10%      |           |         | Power Supply > 0 | Fermented Mushroom Reset | Mushroom Empty / Power        |
| Food Factory        | Corn Rations       | Corn Rations < 70%       | Corn Rations = 100%       | A: Corn Rations Min / RST: Corn Rations Max             | Corn > 10%          |           |         | Power Supply > 0 | Corn Rations Reset       | Corn Empty / Power            |
| Oil Press           | Canola Oil         | Canola Oil < 70%         | Canola Oil = 100%         | A: Canola Oil Min / RST: Canola Oil Max                 | Canola > 10%        |           |         | Power Supply > 0 | Canola Oil Reset         | Canola Empty / Power          |
| Scavenger Flag/Mine | Scrap Metal        | Scrap Metal < 70%        | Scrap Metal = 100%        | A: Scrap Metal Min / RST: Scrap Metal Max               | Treated Plank > 10% |           |         | Power Supply > 0 | Scrap Metal Reset        | Treated Plank Empty / Power   |
| Lumber Mill         | Plank              | Plank < 70%              | Plank = 100%              | A: Plank Min / RST: Plank Max                           | Log > 10%           |           |         | Power Supply > 0 | Plank Reset              | Log Empty / Power             |
| Gear Workshop       | Gear               | Gear < 70%               | Gear = 100%               | A: Gear Min / RST: Gear Max                             | Plank > 10%         |           |         | Power Supply > 0 | Gear Reset               | Plank Empty / Power           |
| Explosives Factory  | Explosive          | Explosive < 70%          | Explosive = 100%          | A: Explosive Min / RST: Explosive Max                   | Badwater > 10%      |           |         | Power Supply > 0 | Explosive Reset          | Badwater Empty / Power        |
| Explosives Factory  | Firework           | Firework < 70%           | Firework = 100%           | A: Firework Min / RST: Firework Max                     | Badwater > 10%      |           |         | Power Supply > 0 | Firework Reset           | Badwater Empty / Power        |
| Metalsmith          | Metal Parts        | Metal Parts < 70%        | Metal Parts = 100%        | A: Metal Parts Min / RST: Metal Parts Max               | Scrap Metal > 10%   | Log > 10% |         |                  | Metal Parts Reset        | Scrap Metal Empty / Log Empty |

### Advanced Processing

| Building       | Resource          | Min                     | Max                      | Memory (Set-Reset)                                    | Empty 1           | Empty 2          | Empty 3 | Power Meter      | Relay (AND)             | Extra                                     |
| -------------- | ----------------- | ----------------------- | ------------------------ | ----------------------------------------------------- | ----------------- | ---------------- | ------- | ---------------- | ----------------------- | ----------------------------------------- |
| Fermenter      | Fermented Soybean | Fermented Soybean < 70% | Fermented Soybean = 100% | A: Fermented Soybean Min / RST: Fermented Soybean Max | Soybean > 10%     | Canola Oil > 10% |         | Power Supply > 0 | Fermented Soybean Reset | Soybean Empty / Canola Oil Empty / Power  |
| Food Factory   | Algae Rations     | Algae Rations < 70%     | Algae Rations = 100%     | A: Algae Rations Min / RST: Algae Rations Max         | Algae > 10%       | Canola Oil > 10% |         | Power Supply > 0 | Algae Rations Reset     | Algae Empty / Canola Oil Empty / Power    |
| Food Factory   | Eggplant Rations  | Eggplant Rations < 70%  | Eggplant Rations = 100%  | A: Eggplant Rations Min / RST: Eggplant Rations Max   | Eggplant > 10%    | Canola Oil > 10% |         | Power Supply > 0 | Eggplant Rations Reset  | Eggplant Empty / Canola Oil Empty / Power |
| Wood Workshop  | Treated Plank     | Treated Plank < 70%     | Treated Plank = 100%     | A: Treated Plank Min / RST: Treated Plank Max         | Plank > 10%       | Pine Resin > 10% |         | Power Supply > 0 | Treated Plank Reset     | Plank Empty / Pine Resin Empty / Power    |
| Smelter        | Metal             | Metal < 70%             | Metal = 100%             | A: Metal Min / RST: Metal Max                         | Scrap Metal > 10% | Log > 10%        |         | Power Supply > 0 | Metal Reset             | Scrap Metal Empty / Log Empty / Power     |
| Centrifuge     | Extract           | Extract < 70%           | Extract = 100%           | A: Extract Min / RST: Extract Max                     | Badwater > 10%    | Log > 10%        |         | Power Supply > 0 | Extract Reset           | Badwater Empty / Log Empty / Power        |
| Grease Factory | Grease            | Grease < 70%            | Grease = 100%            | A: Grease Min / RST: Grease Max                       | Extract > 10%     | Canola Oil > 10% |         | Power Supply > 0 | Grease Reset            | Extract Empty / Canola Oil Empty / Power  |

### Bot Production

| Building         | Resource   | Min              | Max               | Memory (Set-Reset)                      | Empty 1     | Empty 2     | Empty 3     | Power Meter      | Relay (AND)      | Extra                                          |
| ---------------- | ---------- | ---------------- | ----------------- | --------------------------------------- | ----------- | ----------- | ----------- | ---------------- | ---------------- | ---------------------------------------------- |
| Bot Part Factory | Bot Limbs  | Bot Limbs < 70%  | Bot Limbs = 100%  | A: Bot Limbs Min / RST: Bot Limbs Max   | Plank > 10% | Gear > 10%  |             | Power Supply > 0 | Bot Limbs Reset  | Plank Empty / Gear Empty / Power               |
| Bot Part Factory | Bot Chasis | Bot Chasis < 70% | Bot Chasis = 100% | A: Bot Chasis Min / RST: Bot Chasis Max | Plank > 10% | Metal > 10% |             | Power Supply > 0 | Bot Chasis Reset | Plank Empty / Metal Empty / Power              |
| Bot Part Factory | Bot Heads  | Bot Heads < 70%  | Bot Heads = 100%  | A: Bot Heads Min / RST: Bot Heads Max   | Plank > 10% | Gear > 10%  | Metal > 10% | Power Supply > 0 | Bot Heads Reset  | Plank Empty / Gear Empty / Metal Empty / Power |

### Special Production

| Building       | Resource | Min         | Max         | Memory (Set-Reset)              | Empty 1            | Empty 2          | Empty 3   | Power Meter      | Relay (AND)  | Extra                                                     |
| -------------- | -------- | ----------- | ----------- | ------------------------------- | ------------------ | ---------------- | --------- | ---------------- | ------------ | --------------------------------------------------------- |
| Coffee Brewery | Coffee   | Coffee < 10 | Coffee = 20 | A: Coffee Min / RST: Coffee Max | Coffee Beans > 10% | Canola Oil > 10% | Log > 10% | Power Supply > 0 | Coffee Reset | Coffee Beans Empty / Canola Oil Empty / Log Empty / Power |

---

## Power Generation

| Building     | Resource Counter Empty 1 | Resource Counter Empty 2 | Power Meter | Relay (AND) | Extra                   |
| ------------ | ------------------------ | ------------------------ | ----------- | ----------- | ----------------------- |
| Steam Engine | Water > 40%              | Log > 10%                | Surplus < 0 | Power Meter | Water Empty / Log Empty |

---

## Science Control

| Building        | Science Counter Min | Science Counter Max | Memory (Set-Reset)                | Power Meter | Relay (AND)   | Extra |
| --------------- | ------------------- | ------------------- | --------------------------------- | ----------- | ------------- | ----- |
| Number Cruncher | Science < 5000      | Science > 100000    | A: Science Min / RST: Science Max | Surplus < 0 | Science Reset | Power |

---

## Control Tower

| Building      | Science Counter Min | Power Meter      | Relay (AND)         |
| ------------- | ------------------- | ---------------- | ------------------- |
| Control Tower | Science > 20        | Power Supply > 0 | Science Min / Power |

---

## Population Control

| Building          | Population Counter Min  | Population Counter Max  | Memory (Set-Reset)                                        | Resource Counter Empty 1 | Resource Counter Empty 2 | Resource Counter Empty 3 | Power Meter      | Relay (AND)               | Extra                                                        |
| ----------------- | ----------------------- | ----------------------- | --------------------------------------------------------- | ------------------------ | ------------------------ | ------------------------ | ---------------- | ------------------------- | ------------------------------------------------------------ |
| Contamination Pod | Contaminated Beaver = 1 | Contaminated Beaver > 0 | A: Contaminated Beaver Max / RST: Contaminated Beaver Min | Extract > 10%            |                          |                          | Power Supply > 0 | Contaminated Beaver Reset | Extract Empty / Power                                        |
| Bot               | Unemployed Bot < 10     | Unemployed Bot = 20     | A: Unemployed Bot Min / RST: Unemployed Bot Max           | Bot Limbs > 20%          | Bot Heads > 10%          | Bot Chasis > 10%         | Power Supply > 0 | Unemployed Bot Reset      | Bot Limbs Empty / Bot Heads Empty / Bot Chasis Empty / Power |
