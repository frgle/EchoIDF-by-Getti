# Echo Interface Development Framework (EchoIDF)

**Echo IDF** organiza el desarrollo de interfaces en tres ejes: **Interface, Style y Behavior (ISB)**.  
Esta división refleja cómo se construyen aplicaciones modernas en la web y lo traslada al entorno de Roblox Studio.

---

## 🎯 Objetivo
Separar responsabilidades para que la interfaz sea **clara, consistente y mantenible**, evitando mezclar estructura, apariencia y lógica en un solo lugar.

---

## 🔹 Interface (EchoML)
- **Echo** Markup Language

Representa la **estructura visual**.  
Con EchoML declaras jerárquicamente los elementos de la GUI, al estilo de un lenguaje de marcado.  
> *Qué existe en pantalla.*  

Ejemplo: <code>
Frame({ Name = "App" }, 
  TextLabel({ Text = "Welcome!" })
)</code>

---

## 🔹 Style (EchoIM)
- **Echo** Interface Manager
  
Representa la **apariencia**.  
Con EchoIM aplicas estilos centralizados usando selectores tipo CSS, lo que garantiza consistencia y reutilización.  
> *Cómo se ve en pantalla.*  

Ejemplo: <code>
EIM.style(classSelector("btn-primary"), { 
  BackgroundColor3 = Color3.fromRGB(50,150,250) 
})</code>

---

## 🔹 Behavior (EchoIM)
- **Echo** Interface Manager
  
Representa la **interacción**.  
EchoIM también gestiona eventos desacoplados del árbol visual, vinculando callbacks a elementos mediante selectores.  
> *Cómo se comporta en pantalla.*  

Ejemplo: <code>
EIM.on(attrSelector("btn-primary", true), "MouseButton1Click", function(el) 
  print("pressed") 
end)</code>

---

## 🧭 Aproach
- **Interface** → declarar elementos con un DSL claro.  
- **Style** → definir apariencia de manera global y coherente.  
- **Behavior** → gestionar lógica y eventos sin ensuciar la estructura.  

Este flujo ISB ofrece una experiencia similar al **desarrollo web moderno**, pero optimizada para la creación de GUI en Roblox.

---

- @: A **Getti's** Product
