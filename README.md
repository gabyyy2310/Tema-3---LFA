# Tema-3---LFA
⚙️ Structura principală
1. Gramatica S → aSb | ε
Această gramatică generează șiruri de forma aⁿbⁿ, unde n e un număr natural.

generate_strings()
Generează toate șirurile de lungime maximă specificată, în ordine crescătoare.

derivation_steps(target)
Afișează pașii de derivare pentru un șir dat, dacă acesta poate fi derivat.

is_generated(string)
Verifică dacă un șir este generat de gramatică.

2. Gramatica aⁿbⁿcⁿ predefinită manual
O gramatică simplificată, care conține explicit doar un număr limitat de producții pentru aⁿbⁿcⁿ, cu n între 0 și 5.

generate_anbncn_strings()
Generează toate șirurile de forma aⁿbⁿcⁿ cu lungimea totală până la 15.

is_abc(string)
Verifică dacă un șir dat aparține limbajului aⁿbⁿcⁿ, folosind lista de șiruri generate.

🧪 Exemple de rulare
bash
Copy
Edit
Generated strings:
['', 'ab', 'aabb', 'aaabbb', 'aaaabbbb', 'aaaaabbbbb']

Derivation steps for 'aabb':
S => aSb => aaSbb => aabb

Membership tests:
aabb: True
ab: True
aaabbb: True
abab: False
aaaaaaabbbbbbb: False

Generated abc strings:
['abc', 'aabbcc', 'aaabbbccc', 'aaaabbbbcccc', 'aaaaabbbbbccccc']
True

✅ Cerințe
Python 3.x

Nu sunt necesare biblioteci externe

📝 Notă
Pentru gramatica aⁿbⁿcⁿ s-a folosit o abordare statică (producții explicite), deoarece o gramatică CFG generală pentru acest limbaj nu există (limbajul nu este context-free). Pentru a demonstra asta vom folosi Lema de Pompare pentru CFG-uri. Alegand un cuvant din limbaj cu suficient de multe litere, partea in care "pompam" va avea maxim 2 litere diferite. Atunci, mereu a treia litera va genera o ontradictie (macar una din celelalte creste, iar ea sta pe loc).
