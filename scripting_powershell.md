
Extensão dos arquivos criados no powershell: .ps1

## Criando variáveis

```
# definindo a variável 
$name = "Joao"

# valorando uma variável
#age = 30

#recuperando o valor de uma variável
$name

#definindo múltiplas variáveis em uma única linha
$firstname, $lastname = "John", "Doe"

```

## Definindo condicionais
```
if ($idade -gt 18) {
  Write-Host "Adulto"
} else {
  Write-Host "Adolescente"
}
```

## Switch-Case 

```
$dayOfWeek = Get-Date -Format dddd  # Get the current day of the week in full string format (e.g., "Monday", "Tuesday", etc.)

switch ($dayOfWeek) {
    "Monday" { Write-Host "Today is Monday. Time to start the week!" }
    "Tuesday" { Write-Host "Tuesday! Still a long way to go!" }
    "Wednesday" { Write-Host "It's Wednesday. Halfway through!" }
    "Thursday" { Write-Host "Thursday! Almost there!" }
    "Friday" { Write-Host "Friday! Time to celebrate the weekend!" }
    "Saturday" { Write-Host "Saturday! Enjoy the weekend!" }
    "Sunday" { Write-Host "Sunday! Last day before Monday!" }
    Default { Write-Host "Invalid day of the week." }
}
```
## Loop
```
for ($i = 1; $i -le 10; $i++) {
  Write-Host $i
}
```
## While Loop
```
$i = 1
while ($i -le 10) {
  Write-Host $i
  $i++
}
```

## Do-While Loop
```
$i = 1
do {
  Write-Host $i
  $i++
} while ($i -le 10)
```

## Foreach Loop
```
$names = "John", "Jane", "Doe"
foreach ($name in $names) {
  Write-Host $name
}


```
