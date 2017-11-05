# Swift Fundamentals Closures

    //: Playground - noun: a place where people can play
    
    import UIKit
    
    //---------------------------------------------------------------
    //: Author - Cauê Scalzaretto
    //: Site - http://www.cauescalzaretto.com
    //: GitHub - https://github.com/cauescalzaretto
    //---------------------------------------------------------------
    
    //====================================================================================================
    // CLOSURES
    //====================================================================================================
    
    //Closures são ferramentas para a criação de funções in-line. Com elas podemos criar blocos de códigos que podem atuar como variáveis ou funções.
    
    //Como fazemos com funções e métodos, as closures podem receber parâmetros (argumentos) e também podem possuir um retorno de dados, de qualquer tipo
    
    //{(parametros) -> tipoDeRetorno in //Declarações
    //}
    
    
    // CLOSURE
    
    // Declaração da variável, junto com a função
    var saudacaoNoturna = {() -> () in print("Boa Noite")}
    
    // Exibição do resultado
    saudacaoNoturna()
    
    //\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/
    // EXEMPLO 1
    //\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/
    let names = ["Chris", "Alex", "Ewa", "Barry", "Daniella"]
    
    func backward(_ s1: String, _ s2: String) -> Bool {
        return s1 > s2
    }
    var reversedNames = names.sorted(by: backward)
    
    print(reversedNames)
    
    //\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/
    // EXEMPLO 2
    //\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/
    reversedNames = names.sorted(by: { (s1: String, s2: String) -> Bool in
        return s1 > s2
    })
    
    print(reversedNames)
    
    //\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/
    // EXEMPLO 3
    //\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/
    reversedNames = names.sorted(by: { (s1: String, s2: String) -> Bool in return s1 > s2 } )
    print(reversedNames)
    
    
    //\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/
    // EXEMPLO 4
    //\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/
    reversedNames = names.sorted(by: { s1, s2 in return s1 > s2 } )
    print(reversedNames)
    
    
    //\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/
    // EXEMPLO 5
    //\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/
    reversedNames = names.sorted(by: { s1, s2 in s1 > s2 } )
    print(reversedNames)
    
    
    //\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/
    // EXEMPLO 6
    //\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/
    reversedNames = names.sorted(by: { $0 > $1 } )
    print(reversedNames)
    
    
    //\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/
    // EXEMPLO 7
    //\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/
    reversedNames = names.sorted(by: >)
    print(reversedNames)




