# zadanieDatyPHP

<img width="539" height="144" alt="image" src="https://github.com/user-attachments/assets/d200ec81-1133-4a04-aae3-4890aed5534a" />

<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Daty php</title>
</head>
<body>
    <?php
    // Zadanie 1
        $miesiace = [
            1 => 'Styczeń',
            2 => 'Luty',
            3 => 'Marzec',
            4 => 'Kwiecień',
            5 => 'Maj',
            6 => 'Czerwiec',
            7 => 'Lipiec',
            8 => 'Sierpień',
            9 => 'Wrzesień',
            10 => 'Październik',
            11 => 'Listopad',
            12 => 'Grudzień'
        ];

        $dzien = date('d');
        $miesiac = $miesiace[date('n')];
        $rok = date('Y');

        echo $dzien . ' ' . $miesiac . ' ' . $rok;
        echo "<br><br>";

    // Zadanie 2 - dzień tygodnia po polsku
        $dni_tygodnia = [
            1 => 'Poniedziałek',
            2 => 'Wtorek',
            3 => 'Środa',
            4 => 'Czwartek',
            5 => 'Piątek',
            6 => 'Sobota',
            7 => 'Niedziela'
        ];

        $dzien_tygodnia = $dni_tygodnia[date('N')];
        $dzien_liczba = date('d');
        $miesiac_nazwa = date('n');
        $rok_liczba = date('Y');

        echo $dzien_tygodnia . ', ' . $dzien_liczba . '.' . $miesiac_nazwa . '.' . $rok_liczba;
        echo "<br><br>";

    // Zadanie 3 - dni upłynęło od początku roku i dni do końca
        $dni_uplynelo = date('z') + 1;
        $liczba_dni_w_roku = date('L') ? 366 : 365;
        $dni_do_konca = $liczba_dni_w_roku - $dni_uplynelo;

        echo "Od początku roku upłynęło: <strong>" . $dni_uplynelo . " dni</strong><br>";
        echo "Do końca roku pozostało: <strong>" . $dni_do_konca . " dni</strong>";
    ?>
</body>
</html>
