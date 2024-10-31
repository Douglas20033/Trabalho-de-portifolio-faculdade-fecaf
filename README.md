CREATE TABLE Curso (
    ID_Curso INT PRIMARY KEY,
    Nome_Curso VARCHAR(100) NOT NULL,
    Duracao INT NOT NULL
);

CREATE TABLE Aluno (
    ID_Aluno INT PRIMARY KEY,
    Nome VARCHAR(100) NOT NULL,
    Data_Nascimento DATE NOT NULL,
    Curso_ID INT,
    FOREIGN KEY (Curso_ID) REFERENCES Curso(ID_Curso)
);

CREATE TABLE Professor (
    ID_Professor INT PRIMARY KEY,
    Nome VARCHAR(100) NOT NULL,
    Disciplina VARCHAR(100) NOT NULL,
    Contato VARCHAR(100)
);

CREATE TABLE Matéria (
    ID_Materia INT PRIMARY KEY,
    Nome VARCHAR(100) NOT NULL,
    Carga_Horaria INT NOT NULL,
    Professor_ID INT,
    FOREIGN KEY (Professor_ID) REFERENCES Professor(ID_Professor)
);
