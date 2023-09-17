#Fundamentals 
StringBuilder sb = new StringBuilder();
sb.Append("a");
sb.Append("b");
sb.Append("c");
Console.WriteLine(sb);//abc

sb.AppendLine("a");
sb.AppendLine("b");
sb.AppendLine("c"); Console.WriteLine(sb);//a\nb\nc