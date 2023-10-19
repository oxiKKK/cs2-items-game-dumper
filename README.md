# CS2 items_game.txt dumper

Personal items_game.txt CS2 python dumper. Right now the utility is able to generate a c++ file with a list of all items, their definition indexes and how much they cost in-game.

# Usage

```
python main.py test/items_game.txt -d items
```

# Output

```c++
// file generated by CS2 items_game.txt dumper on 2023-10-15 11:20:59.573140
// 
// input file: test/items_game.txt
// 1704 items

struct item_t
{
	// item name
	const char* name{nullptr};
	// item price, how much does it cost in-game;
	int32_t cost{-1};
	// weapon type string;
	const char* weapon_type{nullptr};
};

std::unordered_map<size_t, item_t> g_definition_item_list =
{
	{ 0, { "default", 0, "" } },
	{ 1, { "weapon_deagle", 700, "Pistol" } },
	{ 2, { "weapon_elite", 300, "Pistol" } },
	{ 3, { "weapon_fiveseven", 500, "Pistol" } },
	{ 4, { "weapon_glock", 200, "Pistol" } },
	{ 7, { "weapon_ak47", 2700, "Rifle" } },
	{ 8, { "weapon_aug", 3300, "Rifle" } },
	{ 9, { "weapon_awp", 4750, "SniperRifle" } },
	// ...
};
```