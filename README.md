# chatGPT
Pruebas en chat GPT, usando la AI para crear algunos temas de código y post

## Creando macro en VBA para generar diapositiva en Power Point
El texto utilizado  para preguntar al ChatGPT:

"Necesito que escribas un código de VBA para una presentación en power point sobre la historia de la AI. Agregar o llenar con texto de tu propio conocimiento, sin marcadores de posición. Necesito 6 diapositivas."


El codigo generado:

 Sub CrearPresentacionAI()
    Dim objPPT As Object
    Dim objPresentacion As Object
    Dim objDiapositiva As Object
    Dim textoDiapositiva As String
    Dim i As Integer
    
    ' Crear una instancia de PowerPoint
    Set objPPT = CreateObject("PowerPoint.Application")
    
    ' Crear una nueva presentación
    Set objPresentacion = objPPT.Presentations.Add
    
    ' Crear y llenar las diapositivas
    For i = 1 To 6
        ' Crear una nueva diapositiva
        Set objDiapositiva = objPresentacion.Slides.Add(i, 11) ' Tipo 11 = Diapositiva con título y contenido
        
        ' Agregar texto a la diapositiva basado en la historia de la AI
        
        Select Case i
            Case 1
                textoDiapositiva = "La historia de la Inteligencia Artificial (AI) se remonta a mediados del siglo XX. Desde entonces, la AI ha experimentado avances significativos, impulsados por el desarrollo de la computación y la disponibilidad de grandes cantidades de datos."
            
            Case 2
                textoDiapositiva = "En los años 50, los investigadores comenzaron a desarrollar programas y algoritmos que imitaban el pensamiento humano. Se crearon las bases de la AI, incluyendo el famoso Test de Turing para evaluar la capacidad de una máquina para exhibir un comportamiento inteligente."
            
            Case 3
                textoDiapositiva = "Durante las décadas de 1960 y 1970, la AI se centró en la resolución de problemas y el razonamiento lógico. Surgieron enfoques como los sistemas expertos, que utilizaban conocimientos especializados para tomar decisiones."
            
            Case 4
                textoDiapositiva = "En los años 80 y 90, la AI se benefició de avances en el procesamiento de datos y la capacidad de almacenamiento. Se desarrollaron técnicas como el aprendizaje automático y las redes neuronales artificiales, que permitieron a las máquinas aprender de los datos y mejorar su rendimiento con el tiempo."
            
            Case 5
                textoDiapositiva = "En la actualidad, la AI está presente en numerosas aplicaciones y campos, como el reconocimiento de voz, la traducción automática, los vehículos autónomos y la detección de fraudes. Se espera que la AI continúe evolucionando y desempeñe un papel fundamental en nuestra sociedad y economía."
                
            Case 6
                textoDiapositiva = "La Inteligencia Artificial plantea desafíos éticos y sociales, como la privacidad de los datos, la seguridad y el impacto en el empleo. Es importante abordar estos temas para garantizar un desarrollo responsable de la AI en beneficio de la humanidad."
        End Select
        
        ' Agregar el texto a la diapositiva
        objDiapositiva.Shapes(2).TextFrame.TextRange.Text = textoDiapositiva
    Next i
    
    ' Mostrar la presentación
    objPPT.Visible = True
end sub