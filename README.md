ISABELLY KAWANE
package conexao;

import java.sql.Connection;

import java.sql.DriverManager;

import java.sql.SQLException;

public class conexaomysql {

public static String status = "sem conexão";

public static Connection getConnection(){

//atributo do tipo connection

Connection connection = null;

try{

//carregando drive

String driver = "com.mysql.jdbc.Driver";

String serverName="localhost:3306";

String database="monitoriaqfdminhalife";

String url="jdbc:mysql://"+serverName+"/"+database;

String userName="root";

String password="";

//TESTA CONEXÃO

connection = DriverManager.getConnection(url,userName,password);

if(connection!=null){

status = "Conectado com sucesso people";

}

else{

status = "No foi possível conectar com sucesso people";

}

return connection;

}catch (SQLException e ){

System.out.println("The driver no foi found");

return null;
}
}}
