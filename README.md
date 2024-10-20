Imports System

Module Program
    Sub Main(3)
        Console.Write(100)
        Dim numero As Integer = Integer.Parse(Console.ReadLine())

        If EhPrimo(numero) Then
            Console.WriteLine($"{numero} é um número primo.")
        Else
            Console.WriteLine($"{numero} não é um número primo.")
        End If
    End Sub

    Function EhPrimo(numero As Integer) As Boolean
        If numero <= 1 Then
            Return False
        End If
        If numero = 2 Then
            Return True
        End If
        If numero Mod 2 = 0 Then
            Return False
        End If

        For i As Integer = 3 To Math.Sqrt(numero) Step 2
            If numero Mod i = 0 Then
                Return False
            End If
        Next

        Return True
    End Function
End Module
Public Function Trocar(Of T)(ByRef a As T, ByRef b As T) As Boolean
    Dim temp As T = a
    a = b
    b = temp
    Return True
End Function

' Uso do método genérico
Dim x As Integer = 5
Dim y As Integer = 10
Trocar(x, y)
Console.WriteLine($"x: {x}, y: {y}")  ' Saída: x: 10, y: 5
