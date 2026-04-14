# Exercícios 

1. Escreva um código onde o usuário entra com um número e seja gerada a tabuada de 1 até 10 desse número;

## Solução EXE01
        var scanner = new Scanner(System.in);
        System.out.println("informe um numero");
        var numero = scanner.nextInt();

        for(var i = 1; i <= 10; i++){
            System.out.println(i  * numero);
        }

2. Escreva um código onde o usuário entra com sua altura e peso, seja feito o calculo do seu IMC(IMC = peso/(altura * altura)) e seja exibida a mensagem de acordo com o resultado:
   - Se for menor ou igual a 18,5 "Abaixo do peso";
   - se for entre 18,6 e 24,9 "Peso ideal";
   - Se for entre 25,0 e 29,9 "Levemente acima do peso";
   - Se for entre 30,0 e 34,9 "Obesidade Grau I";
   - Se for entre 35,0 e 39,9 "Obesidade Grau II (Severa)";
   - Se for maior ou igual a 40,0 "Obesidade III (Mórbida)";

## Solução EXE02
        var scanner = new Scanner(System.in);

        System.out.println("informe altura");
        var altura = scanner.nextDouble();

        System.out.println("informe peso");
        var peso = scanner.nextDouble();

        var IMC = peso/(altura * altura);

        if (IMC <= 18.5){
            System.out.println(IMC + " Abaixo do peso");
        } else if (IMC >= 18.6 && IMC <= 24.9) {
            System.out.println(IMC + " Peso ideal");
        } else if (IMC >= 25 && IMC <= 29.9) {
            System.out.println(IMC + " Levemente acima do peso");
        } else if (IMC >= 30 && IMC <= 34.9) {
            System.out.println(IMC + " Obesidade Grau I");
        } else if (IMC >= 35 && IMC <= 39.9) {
            System.out.println(IMC + " Obesidade Grau II(Severa");
        } else if (IMC >= 40) {
            System.out.println(IMC + " Obesidade III (Mórbida)");
        }

3. Escreva um código que o usuário entre com um primeiro número, um segundo número maior que o primeiro e escolhe entre a opção par e impar, com isso o código deve informar todos os números pares ou ímpares (de acordo com a seleção inicial) no intervalo de números informados, incluindo os números informados e em ordem decrescente;

## Solução EXE03

var scanner = new Scanner(System.in);

        System.out.println("informe primeiro numero");
        var num1 = scanner.nextInt();

        System.out.println("informe segundo numero maior que o primeiro");
        var num2 = scanner.nextInt();

        if(num1 >= num2){
            System.out.println("O segundo número deve ser maior que o primeiro!");
            return;
        }

        System.out.println("Digite a opção: 'par' ou 'impar'");
        var opcao = scanner.next();

        for(var i = num2; i >= num1; i--){
            if(opcao.equalsIgnoreCase("par") && (i % 2 == 0)){
                System.out.println(i + "");
            } else if (opcao.equalsIgnoreCase("impar") && (i % 2 != 0)) {
                System.out.println(i + "");
            }
        }

4. Escreva um código onde o usuário informa um número inicial, posteriormente irá informar outros N números, a execução do código irá continuar até que o número informado dividido pelo primeiro número tenha resto diferente de  0 na divisão, números menores que o primeiro número devem ser ignorados

## Solução EXE04 - 01 
        
        var scanner = new Scanner(System.in);

        System.out.println("informe um numero");
        var num1 = scanner.nextInt();
        var keepVerify = true;

        while (keepVerify){
            System.out.println("informe o numero para verificação");
            var toVerify = scanner.nextInt();

            if (toVerify < num1){
                System.out.printf("informe o numero maior que %s \n", num1);
                continue;
            }

            var result = toVerify % num1;
            keepVerify = result == 0;
            System.out.printf("%s %% %s = %s \n", toVerify, num1, result);
        }

## Solução EXE04 - 02

        var scanner = new Scanner(System.in);

        System.out.println("informe um numero");
        var num1 = scanner.nextInt();

        while (true){
            System.out.println("informe o numero para verificação");
            var toVerify = scanner.nextInt();

            if (toVerify < num1){
                System.out.printf("informe o numero maior que %s \n", num1);
                continue;
            }

            var result = toVerify % num1;
            System.out.printf("%s %% %s = %s \n", toVerify, num1, result);
            if(result != 0) break;
        }
