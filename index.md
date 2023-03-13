In this report, I will show three options of the command grep.

-r or --recursive: Recursively search subdirectories listed
-----
Example1
-----
```
[cs15lwi23ald@ieng6-203]:skill-demo1-server:486$ grep -r Rogativa
skill-demo1-data/written_2/travel_guides/berlitz2/PuertoRico-WhereToGo.txt:Behind the museum are a number of other important attractions. Take Calle las Monjas toward San Juan Bay. After a short distance you’ll arrive at the western wall and a small square, Plazuela de la Rogativa, with a bronze statue commemorating the torchlight religious procession, or rogativa, that saved the city in 1797. It’s believed that the lights held by the bishop and the women of the city fooled the British forces in the bay into assuming that Spanish reinforcements had arrived. The British fled empty-handed.
skill-demo1-data/written_2/travel_guides/berlitz2/PuertoRico-WhereToGo.txt:Walk back toward the Plazuela de la Rogativa and peer over the city wall, which rises over 100 ft (301⁄2 m) at this point. The plain façade is broken by the San Juan Gate, which was once the only entrance to the city from the old port. The gate was constructed in 1639, and the walls were completed in 1641. Every person who traveled across the Atlantic from Spain would enter through this narrow passage — many would make their way directly to the Cathedral to give thanks for a safe arrival — and all goods were transported through here. The thick wooden doors are an impressive sight; they were locked and guarded each night but now remain open to allow people to stroll along the seafront.
```

In this example, I used grep -r to search for the word "Rogativa" in the entire current directory and it's subdirectories.

Example2
-----
```
[cs15lwi23ald@ieng6-203]:skill-demo1-server:492$ grep -r "Rogativa\|Plazuela"
skill-demo1-data/written_2/travel_guides/berlitz2/PuertoRico-WhatToDo.txt:Museo del Niño (Plazuela de las Monjas, opposite San Juan Cathedral; Tel. 722-3791). An engaging hands-on museum designed just for children. Open Tue–Thur 9am– 3:30pm, Fri 9am–5pm, Sat and Sun 12:30–5pm.
skill-demo1-data/written_2/travel_guides/berlitz2/PuertoRico-WhereToGo.txt:Facing the cathedral is Plazuela de las Monjas, a tiny square filled with trees, where courting couples and old folks take advantage of the shade. You may also catch the sound of jingling bells signaling that the local ice-cream seller is around. On the north side of the square is the El Convento Hotel, a great place to take a break. The hotel has an interesting history because, as the name suggests, it started life as a convent, in 1651. Unfortunately, as the number of nuns declined, the convent was forced to close, and the building, decaying year by year, played host to the best and busiest brothel in the city. It was also one of the cheapest hotels in town before being rescued and transformed in the early 1990s.
skill-demo1-data/written_2/travel_guides/berlitz2/PuertoRico-WhereToGo.txt:Behind the museum are a number of other important attractions. Take Calle las Monjas toward San Juan Bay. After a short distance you’ll arrive at the western wall and a small square, Plazuela de la Rogativa, with a bronze statue commemorating the torchlight religious procession, or rogativa, that saved the city in 1797. It’s believed that the lights held by the bishop and the women of the city fooled the British forces in the bay into assuming that Spanish reinforcements had arrived. The British fled empty-handed.
skill-demo1-data/written_2/travel_guides/berlitz2/PuertoRico-WhereToGo.txt:Walk back toward the Plazuela de la Rogativa and peer over the city wall, which rises over 100 ft (301⁄2 m) at this point. The plain façade is broken by the San Juan Gate, which was once the only entrance to the city from the old port. The gate was constructed in 1639, and the walls were completed in 1641. Every person who traveled across the Atlantic from Spain would enter through this narrow passage — many would make their way directly to the Cathedral to give thanks for a safe arrival — and all goods were transported through here. The thick wooden doors are an impressive sight; they were locked and guarded each night but now remain open to allow people to stroll along the seafront.
```

In this example, I used grep -r to search for the words "Rogativa" and "Plazuela" at once by dividing them with the symbol "\|".

-i or --ignore-case: Ignore case distinctions in both the pattern and the input files.
-----
Example1
-----
```
skill-demo1-data/written_2/travel_guides/berlitz2/PuertoRico-WhereToGo.txt:Behind the museum are a number of other important attractions. Take Calle las Monjas toward San Juan Bay. After a short distance you’ll arrive at the western wall and a small square, Plazuela de la Rogativa, with a bronze statue commemorating the torchlight religious procession, or rogativa, that saved the city in 1797. It’s believed that the lights held by the bishop and the women of the city fooled the British forces in the bay into assuming that Spanish reinforcements had arrived. The British fled empty-handed.
skill-demo1-data/written_2/travel_guides/berlitz2/PuertoRico-WhereToGo.txt:Walk back toward the Plazuela de la Rogativa and peer over the city wall, which rises over 100 ft (301⁄2 m) at this point. The plain façade is broken by the San Juan Gate, which was once the only entrance to the city from the old port. The gate was constructed in 1639, and the walls were completed in 1641. Every person who traveled across the Atlantic from Spain would enter through this narrow passage — many would make their way directly to the Cathedral to give thanks for a safe arrival — and all goods were transported through here. The thick wooden doors are an impressive sight; they were locked and guarded each night but now remain open to allow people to stroll along the seafront.
```

In this example, I used -i to search for both "rogativa" and "Rogativa".

Example2
-----
```
[cs15lwi23ald@ieng6-203]:skill-demo1-server:495$ grep -r -i Rogativa
skill-demo1-data/written_2/travel_guides/berlitz2/PuertoRico-WhereToGo.txt:Behind the museum are a number of other important attractions. Take Calle las Monjas toward San Juan Bay. After a short distance you’ll arrive at the western wall and a small square, Plazuela de la Rogativa, with a bronze statue commemorating the torchlight religious procession, or rogativa, that saved the city in 1797. It’s believed that the lights held by the bishop and the women of the city fooled the British forces in the bay into assuming that Spanish reinforcements had arrived. The British fled empty-handed.
skill-demo1-data/written_2/travel_guides/berlitz2/PuertoRico-WhereToGo.txt:Walk back toward the Plazuela de la Rogativa and peer over the city wall, which rises over 100 ft (301⁄2 m) at this point. The plain façade is broken by the San Juan Gate, which was once the only entrance to the city from the old port. The gate was constructed in 1639, and the walls were completed in 1641. Every person who traveled across the Atlantic from Spain would enter through this narrow passage — many would make their way directly to the Cathedral to give thanks for a safe arrival — and all goods were transported through here. The thick wooden doors are an impressive sight; they were locked and guarded each night but now remain open to allow people to stroll along the seafront.
```
In this example, I used -i to search for both "rogativa" and "Rogativa". You can see that it give the same result no matter if you type **grep -r -i Rogativa** or **grep -r -i rogativa**

-n or --line-number: Prefix each line of output with the 1-based line number within its input file.
-----
Example1
-----

```
[cs15lwi23ald@ieng6-203]:skill-demo1-server:497$ grep -r -n Rogativa
skill-demo1-data/written_2/travel_guides/berlitz2/PuertoRico-WhereToGo.txt:28:Behind the museum are a number of other important attractions. Take Calle las Monjas toward San Juan Bay. After a short distance you’ll arrive at the western wall and a small square, Plazuela de la Rogativa, with a bronze statue commemorating the torchlight religious procession, or rogativa, that saved the city in 1797. It’s believed that the lights held by the bishop and the women of the city fooled the British forces in the bay into assuming that Spanish reinforcements had arrived. The British fled empty-handed.
skill-demo1-data/written_2/travel_guides/berlitz2/PuertoRico-WhereToGo.txt:30:Walk back toward the Plazuela de la Rogativa and peer over the city wall, which rises over 100 ft (301⁄2 m) at this point. The plain façade is broken by the San Juan Gate, which was once the only entrance to the city from the old port. The gate was constructed in 1639, and the walls were completed in 1641. Every person who traveled across the Atlantic from Spain would enter through this narrow passage — many would make their way directly to the Cathedral to give thanks for a safe arrival — and all goods were transported through here. The thick wooden doors are an impressive sight; they were locked and guarded each night but now remain open to allow people to stroll along the seafront.
```
In this example, I used -n to show the line number of each "Rogativa" in their files.

Example2
-----
```
[cs15lwi23ald@ieng6-203]:skill-demo1-server:499$ grep -r -n Plazuela
skill-demo1-data/written_2/travel_guides/berlitz2/PuertoRico-WhatToDo.txt:102:Museo del Niño (Plazuela de las Monjas, opposite San Juan Cathedral; Tel. 722-3791). An engaging hands-on museum designed just for children. Open Tue–Thur 9am– 3:30pm, Fri 9am–5pm, Sat and Sun 12:30–5pm.
skill-demo1-data/written_2/travel_guides/berlitz2/PuertoRico-WhereToGo.txt:26:Facing the cathedral is Plazuela de las Monjas, a tiny square filled with trees, where courting couples and old folks take advantage of the shade. You may also catch the sound of jingling bells signaling that the local ice-cream seller is around. On the north side of the square is the El Convento Hotel, a great place to take a break. The hotel has an interesting history because, as the name suggests, it started life as a convent, in 1651. Unfortunately, as the number of nuns declined, the convent was forced to close, and the building, decaying year by year, played host to the best and busiest brothel in the city. It was also one of the cheapest hotels in town before being rescued and transformed in the early 1990s.
skill-demo1-data/written_2/travel_guides/berlitz2/PuertoRico-WhereToGo.txt:28:Behind the museum are a number of other important attractions. Take Calle las Monjas toward San Juan Bay. After a short distance you’ll arrive at the western wall and a small square, Plazuela de la Rogativa, with a bronze statue commemorating the torchlight religious procession, or rogativa, that saved the city in 1797. It’s believed that the lights held by the bishop and the women of the city fooled the British forces in the bay into assuming that Spanish reinforcements had arrived. The British fled empty-handed.
skill-demo1-data/written_2/travel_guides/berlitz2/PuertoRico-WhereToGo.txt:30:Walk back toward the Plazuela de la Rogativa and peer over the city wall, which rises over 100 ft (301⁄2 m) at this point. The plain façade is broken by the San Juan Gate, which was once the only entrance to the city from the old port. The gate was constructed in 1639, and the walls were completed in 1641. Every person who traveled across the Atlantic from Spain would enter through this narrow passage — many would make their way directly to the Cathedral to give thanks for a safe arrival — and all goods were transported through here. The thick wooden doors are an impressive sight; they were locked and guarded each night but now remain open to allow people to stroll along the seafront.
[cs15lwi23ald@ieng6-203]:skill-demo1-server:500$
```
In this example, I used -n to show the line number of each "Plazuela" in their files.
