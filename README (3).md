# KMP String Search – C#

Minimal, allocation-free implementation of the Knuth–Morris–Pratt (KMP)
algorithm for fast substring matching.

* **O(n)** time, **O(m)** memory
* Single file, MIT license, .NET 6+
* Useful for DNA/protein search, log scanning, editors, parsers, etc.

## Quick start
```csharp
using Kmp;

var text    = "ababcabcabababd";
var pattern = "ababd";

int idx = KnuthMorrisPratt.First(text, pattern);   // → 10
var all = KnuthMorrisPratt.Search(text, "ab");     // → [0,2,5,7,10,12]
Console.WriteLine(idx);
Console.WriteLine(string.Join(", ", all));
