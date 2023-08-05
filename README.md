# Greeting
In this application, when selecting a specific country, a greeting is presented for a Programmer in the language of the selected country. If the mouse is placed over each country without selecting it, the MouseHover event, well known in web development for those who have worked with Javascript, is generated. 

Visual Basic.NET:
Public Class Form1

    Private Sub Form1_Load(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles MyBase.Load

        lstCuadroPais.Items.Add("Paises Bajos")
        lstCuadroPais.Items.Add("Portugal")
        lstCuadroPais.Items.Add("Alemania")
        lstCuadroPais.Items.Add("Italia")

    End Sub

    Private Sub lstCuadroPais_MouseHover(ByVal sender As Object, ByVal e As System.EventArgs) Handles lstCuadroPais.MouseHover

        If lstCuadroPais.SelectedIndex < 0 Or lstCuadroPais.SelectedIndex > 4 Then
            etiSaludos.Text = "Por Favor haga Clic en el nombre del Pais"
        End If

    End Sub

    Private Sub lstCuadroPais_SelectedIndexChanged(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles lstCuadroPais.SelectedIndexChanged

        etiSaludos.Text = lstCuadroPais.Text
        Select Case lstCuadroPais.SelectedIndex
            Case 0
                etiSaludos.Text = "Hallo, Programmeur"
            Case 1
                etiSaludos.Text = "Olá, Programador"
            Case 2
                etiSaludos.Text = "Hallo, Programmierer"
            Case 3
                etiSaludos.Text = "Ciao, Programmatore"
        End Select
    End Sub

    Private Sub btnQuit_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles btnQuit.Click
        End
    End Sub
End Class
