/* 
@autor Wesley de Carvalho Souza
programa para calcular ajuste salarial
*/

public class Pessoa {
     
    private int idade;
    private String nome;
    
    
//metodo construtor
    public Pessoa(String nome, int idade) {
       this.setNome(nome);
       this.setIdade(idade);
    }
       //metodo de get/set 
       //encapsulamento
    public String getNome() {
        return nome;
    }
    
    public void setNome(String nome) {
        this.nome = nome;
    }

    public int getIdade() {
        return idade;
    }

    public void setIdade(int idade) {
        this.idade = idade;
    }

}
public class Funcionario extends Pessoa {
    double salario;

    public Funcionario(String nome, int idade, double salario) {
        super(nome, idade);
        this.setSalario(salario);
    }
    
    public double getSalario() {
        return salario;
    }

    public void setSalario(double salario) {
        this.salario = salario;
    }
    //metodo
    public double calcularReajuste (double porcentagem){
        return this.salario + (this.salario * porcentagem / 100);
    }

    String get() {
        throw new UnsupportedOperationException("Not supported yet."); // Generated from nbfs://nbhost/SystemFileSystem/Templates/Classes/Code/GeneratedMethodBody
    }
}
public class UsaFuncionario {
    public static void main(String[] args) {
        
        Funcionario f1 = new Funcionario("Lozano", 37, 1000);
        
        System.out.println("Nome: " + f1.getNome()+
                          "\nIdade: " + f1.getIdade() + 
                          "\nSalario: " + f1.getSalario())  ;
    } 
}

