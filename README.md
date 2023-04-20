# Criando conexão node e MYSQL
    * npm init -y
    * npm i mysql2
# Arquivos padrões
    * README.md
    * .gitignore
# Primeira conexão
    const mysql = require('mysql2')

    const connetion = mysql.createConnection({
        host: 'localhost',
        user: 'root',
        password: '',
        database: 'teste2023'
    })

    connetion.query('select * from produtos', (err, results, fields) => {
        console.log(err, results, fields)
    })
# Conexao com Promise