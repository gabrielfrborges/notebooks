
# Prática 03
### Lista de ES I | Prof. Juliana
---
#### Aluno: Gabriel Borges && Gabriel Mendes (ADS 2ºB)  

1. Escreva a a saída desta estrutura de repatição e seu teste de mesa:  

```
int a =10, s =0;
while(a < 18) {
    // Parada do teste de mesa
    if(a%2 ==0) {
        s++;
    }
    a++;
}
System.out.println(s);
```

**a**|**s**
---|---
10|0
11|1
12|1
13|2
14|2
15|3
16|3
17|4

*Saída:  4*  

2. Escreva a a saída desta estrutura de repatição e seu teste de mesa: 
```
int x=0, y=0, z=0;
for(z=0;z<6;z++){
    // Parada do teste de mesa
    if(++x> 4 || ++y >3)
        x++;
System.out.println(x+" "+y);
}
```

**x**|**y**|**z**
---|---|---
0|0|0
1|1|1
2|2|2
3|3|3
5|4|4
7|4|5

*Saída(x y): 9 4*  

3. Escreva a a saída desta estrutura de repatição e seu teste de mesa: 
```
int num= 20, r= 0;
// Teste de mesa 01
r = (20+2)/2;
// Teste de mesa 02
if(r>13)
    System.out.println(num);
else
    System.out.println(r += 2);
// Teste de mesa 03
```

**num**|**r**
---|---
20|0
20|11
20|13

*Saída: 13*  

4.  Responda as questões a seguir a respeito Conceitos de Orientação a Objetos e dê um exemplo para cada um deles:
    * Classes  
    > Classe é uma abstração de um conjunto de objetos com características em comum.
    >*Por exemplo:  As classes Cachorro e Janela são abstrações de um conjuto de objetos com a caratéristicas em comum, cachorros e janelas respectivamente*
    
    * Objetos   
    >  Em Programação orientada a objetos, objetos são instancias de uma classe, combinação dos valores que compõe a classe.
    >  *Por exemplo:  Uma variável "cookie" é um objeto da classe Cachorro, assim como "janela_da_sala" é um objeto da classe Janela*  
    
    * Atributos   
    >  Atributos são propriedades de um objeto, moldado em uma classe e específicado para cada um dos objetos quando inicializados.
    >  *Por exemplo:  Uma classe Cachorro tem o atributo "peso", e uma Janela "cor".*  
    
    * Métodos  
    >  Médotodos são subrotinas associadas com uma classe, ou ainda atividades relacionadas com a classe. 
    >*Por exemplo: uma classe Cachorro teria um método "latir", uma Janela teria o método "abrir" e"fechar".*

5. Usando Java:  
  * Crie uma classe conforme a seguinte  

|**Disciplina**|
|--------------|
|\- nome       |
|\- código     |
|\- descrição  |
|              |
|\+ imprimir   |

   * A classe disciplina deve conter os métodos getters e setters para cada atributo.  
   * A classe disciplina deve conter o constructor.  


```
public class Disciplina {
    private String nome;
    private int codigo;
    private String descricao;

    Disciplina(String nome, int cdg, String desc){
        this.nome = nome;
        this.codigo = cdg;
        this.descricao = desc;
    }

    public boolean setnome(String nome) {
        if(nome != "Claudio") {
            this.nome = nome;
            return true;
        }
        return false;
    }
    public String getnome() {
        return this.nome;
    }

    public boolean setcogigo(int cdg) {
        if(cdg < 1000) {
            this.codigo = cdg;
            return true;
        }
        return false;
    }
    public int getcodigo() {
        return this.codigo;
    }

    public boolean setdesc(String desc) {
        if(desc.length() > 5) {
            this.descricao = desc;
            return true;
        }
        return false;
    }
    public String getdesc() {
        return this.descricao;
    }

    public void imprimir() {
        System.out.println(this.nome);
        System.out.println(this.codigo);
        System.out.println(this.descricao);
    }
}
```


* Criar a classe Teste que conterá o método principal.  Criar pelo menos 2 objetos e imprimi-los.  

	```
	public class praticaLauncher {

		public static void main(String[] args) {
			Disciplina math = new Disciplina("Mathematics", 0, "Mother of all sciences");
			math.imprimir();
			math.setcogigo(3);
			math.imprimir();
			System.out.println();
			Disciplina es1 = new Disciplina("Software Enginering 1", 2, "Very cool subject");
			es1.imprimir();
			es1.setnome("Software Enginering 2");
			es1.imprimir();
		}

	}
	```
	*Saída:*

	```
	Mathematics
	0
	Mother of all sciences
	Mathematics
	3
	Mother of all sciences

	Software Enginering 1
	2
	Very cool subject
	Software Enginering 2
	2
	Very cool subject
	```
6.  Analíse o código a seguir e responda;
	
```
public class praticaLauncher {

    public static void main(String[] args) {
        Produto produto;
        Item item_produto;

        produto = new Produto(101, "Caderno", 10);
        item_produto =new Item(1, 30, 0, produto);

        System.out.println("O valor do Item:"+ item_produto.calcularValor());
        }
}  
```
   - Qual o comando que cria objeto? Quais objetos estão sendo criados na classe Principal?
      		> O comando que cria um novo objeto é o `new`,  os objetos sendo criados são o classe *Produto* e *Item*.
   - O que são variáveis de referência? Existem variáveis de referência na classe Principal? Caso sim, quais
     >  Váriaveis de refenrência são ponteiros para endereços de memória onde está alocado o objeto referenciado. As variáveis de referência na  classe Principal são : `produto` e `item_produto`.
	

