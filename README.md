import java.util.Scanner;


public class SistemaEscolar {
   public static void main(String[] args) {
      Scanner scanner = new Scanner(System.in);
      double[] notas = new double[8];

    //Receber as 8 notas anuais 
    System.out.println("Digite as 8 notas anuais:");
    for (int i = 0;i < 8; i++) {
       System.out.print((i + 1) + "° Nota: ");
       notas[i] = scanner.nestxDouble();
    }

    // Calcular médias bimestrais (cada bimestre tem 2 notas)
    double bimestre1 = (notas[0] + notas[1]) / 2;
    double bimestre2 = (notas[2] + notas[3]) / 2;
    double bimestre3 = (notas[4] + notas[5]) / 2;
    double bimestre4 = (notas[6] + notas[7]) / 2;


    // Calcular médias semestrais (cada semestre tem 2 bimestres)
    double semestre1 = (bimestre1 + bimestre2) / 2;
    double bimestre2 = (bimestre3 + bimestre4) / 2;


    // Calcular média final (média dos dois semestres)
    double mediaFinal = (semestre1 + semestre2) / 2;

    // Apresentar os resultados 
    System.out.println("\nResultado:");
    System.out.printf("1° Bimestre: %.if\n",bimestre1);
    System.out.printf("2° Bimestre: %.if\n",bimestre2);
    System.out.printf("1° Semestre: %.if\n",semestre1);
    System.out.printf("3° Bimestre: %.if\n",bimestre3);
    System.out.printf("4° Bimestre: %.if\n",bimestre4);
    System.out.printf("2° Semestre: %.if\n",semestre2);
    System.out.printf("Média Final: %.if\n",mediaFinal);

    scanner.close()

  }
}
