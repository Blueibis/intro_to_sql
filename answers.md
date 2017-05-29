SELECT * FROM robots
WHERE source = ‘The Hitchhiker’‘s Guide to the Galaxy’;

SELECT * FROM robots
WHERE personality = ‘anxious’;

SELECT name FROM recipes
WHERE nut_free = true;

SELECT COUNT(name)
FROM recipes
WHERE gluten_free = true AND vegetarian = false;

SELECT name FROM animals
WHERE number_of_legs in(SELECT MAX(number_of_legs) from animals);

SELECT name FROM board_games
WHERE mins_to_play in (SELECT MIN(mins_to_play) from board_games);

SELECT name FROM recipes
WHERE minutes_required in (SELECT MAX(minutes_required) from recipes);

SELECT * FROM robots
WHERE name LIKE ‘M%‘;

SELECT COUNT(name) FROM board_games
WHERE max_players >= 8 AND min_players <= 8;

SELECT name from animals
WHERE swimming = true AND egg_laying = true;

SELECT name from animals
WHERE swimming = true AND egg_laying = true AND flying = false;

SELECT name from board_games
WHERE max_players in (SELECT MAX(max_players) FROM board_games);
