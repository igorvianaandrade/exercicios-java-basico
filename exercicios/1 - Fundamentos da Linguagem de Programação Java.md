 # Exercícios 

1. Escreva um código que receba o nome e o ano de nascimento de alguém e imprima na tela a seguinte mensagem: "Olá 'Fulano' você tem 'X' anos"

        var scanner = new Scanner(System.in);
        var currentYear = OffsetDateTime.now().getYear();

        System.out.println("Qual o seu nome?");
        String name = scanner.next();

        System.out.println("Qual o seu ano de nascimento?");
        var bornYear = scanner.nextInt();

        var age = currentYear - bornYear;

        System.out.printf("Olá %s você tem %s anos", name, age);

2. Escreva um código que receba o tamanho do lado de um quadrado, calcule sua área e exiba na tela
   - fórmula: área=lado X lado

        var scanner = new Scanner(System.in);

        System.out.println("Lado do quadrado:");
        var side = scanner.nextInt();

        var area = side * side;

        System.out.printf("A area do quadrado de lado %s é igual a %s", side, area);


3. Escreva um código que receba a base e a alturade um retângulo, calcule sua área e exiba na tela
   - fórmula: área=base X altura

        var scanner = new Scanner(System.in);

        System.out.println("Escreva a base do retangulo:");
        var base = scanner.nextInt();

        System.out.println("Escreva a altura do retangulo:");
        var height = scanner.nextInt();

        var resultArea = base * height;

        System.out.printf("A area do retangulo de base %s e altura %s é igual a %s", base, height, resultArea);

4. Escreva um código que receba o nome e a idade de 2 pessoas e imprima a diferença de idade entre elas

        var scanner = new Scanner(System.in);

        System.out.println("Pessoa 01 - Escreva seu nome: ");
        var personOne = scanner.next();

        System.out.println("Pessoa 01 - Escreva sua idade: ");
        var ageOne = scanner.nextInt();

        System.out.println("Pessoa 02 - Escreva seu nome: ");
        var personTwo = scanner.next();

        System.out.println("Pessoa 02 - Escreva sua idade: ");
        var ageTwo = scanner.nextInt();

        var ageDifference = ageOne - ageTwo;

        System.out.printf("%s com idade %s tem %s ano(s) de diferença de %s com idade %s", personOne, ageOne, ageDifference, personTwo, ageTwo);
