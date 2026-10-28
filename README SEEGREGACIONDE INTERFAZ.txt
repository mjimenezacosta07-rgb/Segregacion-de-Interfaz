principio de segregacion de interfaces

este principio dice que una clase no debe tener metodos que no necesita, por eso se usan interfaces pequeñas para que cada clase tenga solo lo que ocupa
un ejemplo es el control del televisor y el del aire acondicionad no tendria sentido que el control del aire tenga botones para cambiar canales


Como se implementa


la clase producto tiene el nombre y el precio de los productos
se crean tres interfaces:

enviable tiene el metodo eviar

remplazable tiene el metodo reemplazar

expirable tiene el metodo expirar
fisico hereda de producto enviable y remplazable porque se puede enviar y reemplazar
digital hereda de producto y expirable porque en este ejemplo se puede vencer
si todos los metodos estuvieran en una sola interfaz digital tendria que implementar enviar y reemplazar aunque no los use y fisico tendria que implementar expirar aunque no lo necesite





Explicacion de los archivos


Producto.h y Producto.cpp

declaran la clase producto con nombre y precio y escriben lo que hacen sus metodos get y set
Enviable.h y Enviable.cpp
declaran la interfaz enviable con el metodo virtual puro enviar el cpp tiene el constructor y el destructor
Remplazable.h y Remplazable.cpp
declaran la interfaz remplazable con el metodo virtual puro reemplazar el cpp tiene el constructor y el destructor
Expirable.h y Expirable.cpp
declaran la interfaz expirable con el metodo virtual puro expirar el cpp tiene el constructor y el destructor

Fisico.h
declara la clase fisco que hereda de producto, enviable y remplazable, agrega el atributo peso y declara sus métodos

Fisico.cpp
escribe lo que hacen getPeso y setPeso enviar devuelve "enviando" y reemplazar devuelve "reemplazando"


Digital.h
declara la clase digital que hereda de producto y expirable, agrega el atributo filepath que es la ruta del archivo y declara sus métodos


Digital.cpp
escribe lo que hacen getFilePath y setFilePath, expirar devuelve "expirado"


Main
crea el producto fisico nintendo y el producto digital game
muestra el nombre del fisico y llama a enviar y reemplazar
muestra el nombre del digital y llama a expirar