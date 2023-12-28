- A [[Variables#Composite Variables | composite data type]] used in programming languages to group together variables of different data types under a single name
- They provide a way to organize related pieces of information into a cohesive unit

! In C "typedef" creates a new variable
```C
typedef char *String;
```

^d74f88

```C
typedef struct {
	String name;
	String number;
} Person;

int main(void) {
	Person max;
	max.name = "Maximillian";
	max.number = "+90 5324325373"
}
```

```CSharp
// From Mythstone -> Gem Generator
[Serializable]
public struct Gem
{
	public GameObject prefab;
	[Range(0f, 100f)] public float probabilityWeight;
	public bool canNotBeGrouped;
}
public List<Gem> gems;
```

