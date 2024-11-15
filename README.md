
## Atividade 15 - Implementando Relacionamento ManyToMany
  
## cessando o Console H2

- Para acessar o console do H2:

        Abra o navegador e vá para http://localhost:8080/h2-console.
        Configure o campo "JDBC URL" como jdbc:h2:mem:testdb, com o username sa e deixe o password em branco.
        Clique em "Connect" para visualizar o banco de dados.

- Controller: Implemente um controlador REST para as seguintes operações:
  
        POST /alunos: Adicionar um novo aluno.
        POST /cursos: Adicionar um novo curso.
        POST /alunos/{id}/cursos/{cursoId}: Matricular um aluno em um curso.
        DELETE /alunos/{id}/cursos/{cursoId}: Remover um aluno de um curso.
        GET /alunos/{id}/cursos: Listar todos os cursos em que um aluno está matriculado.
        GET /cursos/{id}/alunos: Listar todos os alunos matriculados em um curso.

# Endpoints
        Endpoints da CourseController
- Criar um curso

        URL: POST /courses
        Corpo: { "name": "Nome do Curso", ... }
        Retorno: 200 OK com o curso criado.
        Obter curso por ID

        URL: GET /courses/{id}
        Retorno: 200 OK com o curso correspondente.
        Atualizar um curso

        URL: PUT /courses/{id}
        Corpo: { "name": "Novo Nome", ... }
        Retorno: 200 OK com o curso atualizado.
        Deletar um curso

        URL: DELETE /courses/{id}
        Retorno: 204 No Content.
        Listar todos os estudantes de um curso

        URL: GET /courses/{id}/students
        Retorno: 200 OK com a lista de estudantes.
        Buscar curso por nome

        URL: GET /courses/name/{name}
        Retorno: 200 OK com o curso correspondente.
        Endpoints da StudentController
- Criar um estudante

        URL: POST /students
        Corpo: { "name": "Nome do Estudante", ... }
        Retorno: 200 OK com o estudante criado.
        Obter estudante por ID

        URL: GET /students/{id}
        Retorno: 200 OK com o estudante correspondente.
        Atualizar um estudante

        URL: PUT /students/{id}
        Corpo: { "name": "Novo Nome", ... }
        Retorno: 200 OK com o estudante atualizado.
        Deletar um estudante

        URL: DELETE /students/{id}
        Retorno: 204 No Content.
        Listar todos os cursos de um estudante

        URL: GET /students/{id}/courses
        Retorno: 200 OK com a lista de cursos.
        Buscar estudante por email

        URL: GET /students/email/{email}
        Retorno: 200 OK com o estudante correspondente.
        Matricular estudante em um curso

        URL: POST /students/{studentId}/courses/{courseId}
        Retorno: 200 OK com mensagem de sucesso.
        Remover estudante de um curso

        URL: DELETE /students/{studentId}/courses/{courseId}
        Retorno: 204 No Content.
        Testando a API