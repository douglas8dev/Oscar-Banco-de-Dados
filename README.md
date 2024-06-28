# Oscar-Banco-de-Dados
# Oscar 🎞️🏆⭐

### Quantas vezes Natalie Portman foi indicada ao Oscar?

SELECT * FROM indicados_ao_oscar 
WHERE nome_do_indicado = 'Natalie Portman';
return: 3

SELECT COUNT(*) FROM indicados_ao_oscar 
WHERE nome_do_indicado = 'Natalie Portman' AND vencedor = 'true';
apenas 1

### Amy Adams já ganhou algum Oscar?

SELECT COUNT(*) FROM indicados_ao_oscar 
WHERE nome_do_indicado = 'Amy Adams' AND vencedor = 'true';

### A série de filmes Toy Story ganhou um Oscar em quais anos?

SELECT ano_cerimonia, nome_do_filme FROM indicados_ao_oscar 
WHERE nome_do_filme LIKE '%Toy Story%' AND vencedor = 'true';

### A partir de que ano que a categoria "Actress" deixa de existir? 

SELECT min(ano_cerimonia) FROM indicados_ao_oscar
WHERE categoria = 'Actress';


### O primeiro Oscar para melhor Atriz foi para quem? Em que ano?

SELECT ano_cerimonia, nome_do_indicado FROM indicados_ao_oscar 
WHERE categoria like 'Actress' and vencedor = 'true' ORDER BY ano_cerimonia;

### Na coluna/campo "Vencedor", altere todos os valores com "Sim" para 1 e todos os valores "Não" para 0.

UPDATE indicados_ao_oscar
UPDATE indicados_ao_oscar
set vencedor = 1
where vencedor = 'true';
 
UPDATE indicados_ao_oscar
set vencedor = 0
where vencedor = 'false';

### Em qual edição do Oscar "Crash" concorreu ao Oscar?

SELECT DISTINCT cerimonia
FROM indicados_ao_oscar
WHERE nome_do_filme LIKE '%Crash%';


### Bom... dê um Oscar para um filme que merece muito, mas não ganhou.

INSERT INTO indicados_ao_oscar (ano_filmagem, ano_cerimonia, cerimonia, categoria, nome_do_indicado, nome_do_filme, vencedor)
VALUES (2023, 2024, 96, '%', 'Great Film', 'The Great Movie', 'Sim');


### O filme Central do Brasil aparece no Oscar? 

FROM indicados_ao_oscar
WHERE nome_do_filme LIKE '%Central do Brasil%';

### Inclua no banco 3 filmes que nunca foram nem nomeados ao Oscar, mas que merecem ser. 
INSERT INTO indicados_ao_oscar (ano_filmagem,  nome_do_filme, vencedor)
VALUES 
(1987, 'The Wolf of Wall Street', 'Não'),
(2002, 'Cidade de Deus', 'Não'),
(1998, 'Central do Brasil', 'Não');



###  Pensando no ano em que você nasceu: Qual foi o Oscar de melhor filme, Melhor Atriz e Melhor Diretor?

SELECT nome_do_indicado, nome_do_filme, cerimonia
 
-- dar update p atualizar o database
FROM indicados_ao_oscar
 
WHERE categoria IN ('Uma Mente Brilhante', 'Jennifer Connelly', 'David Lean') AND ano_filmagem = 2002 AND vencedor = 'Sim';
tem menu de contexto


