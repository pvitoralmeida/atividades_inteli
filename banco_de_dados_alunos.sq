CREATE TABLE cursos (
  id SERIAL primary key,
  nome text not null,
  classificacao_mec int
);

CREATE TABLE alunos (
  id SERIAL primary key,
  nome text not null,
  turma text not null,
  curso text not null,
  idade int
);

CREATE TABLE matriculas (
  id SERIAL PRIMARY KEY,
  aluno_id INT REFERENCES alunos(id) ON DELETE CASCADE,
  curso_id INT REFERENCES cursos(id) ON DELETE CASCADE
);

INSERT INTO alunos (nome, turma, curso, idade)
VALUES ('Hugo Montan', '15', 'ADM Tech', 20),
       ('Nicolli Venino', '15', 'Engenharia da Computação', 18),
       ('Alessandra Sena', '15', 'Engenharia de Software', 20),
       ('Maria Arielly', '15', 'Engenharia de Software', 19),
       ('Kethlen Martins', '12', 'Engenharia da Computação', 19),
       ('Thulio Bacco', '15', 'Ciência da Computação', 20),
       ('Leunam Oliveira', '17', 'ADM Tech', 19),
       ('João Cardoso', '18', 'Engenharia da Computação', 18),
       ('Lívia Cavalcanti', '15', 'Sistemas de Informação', 18),
       ('Felipe Neves', '15', 'Engenharia de Software', 18);

INSERT INTO cursos (nome, classificacao_mec)
VALUES ('Sistemas de Informação', 5),
       ('Engenharia de Software', 5),
       ('ADM Tech', null),
       ('Engenharia da Computação', 5),
       ('Ciência da Computação', 5);

SELECT * FROM cursos;

INSERT INTO matriculas (aluno_id, curso_id)
VALUES (1, 3),
       (2, 4),
       (3, 2),
       (4, 2),
       (5, 4),
       (6, 5),
       (7, 3),
       (8, 4),
       (9, 1),
       (10, 2);

SELECT a.nome as alunos, c.nome as cursos
FROM matriculas m
JOIN alunos a ON m.aluno_id = a.id
JOIN cursos c ON m.curso_id = c.id;
