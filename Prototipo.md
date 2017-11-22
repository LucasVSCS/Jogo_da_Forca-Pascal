# Jogo da Forca - Pascal
Program Jogo_forca ;

var
resposta: array[1..4] of string;
opcao_menu, opcao_assunto, opcao_dificuldade, pontos: integer;
resp: string;

//Procedimento pro menu principal
procedure menu_principal ();
begin
  writeln ('=================Jogo da Forca===================');
  writeln;
  writeln ('1 ===================Começar=====================');
  writeln;
  writeln ('2 ==================Instruções===================');
  writeln;
  writeln ('3 ====================Loja=======================');
  writeln;
end;

//Procedimento pro menu de assuntos
procedure menu_assuntos();
begin
  writeln ('==================Escolha um assunto=============');
  writeln;
  writeln ('1 ==================Entreterimento===============');
  writeln;
  writeln ('2 ==================Matemática===================');
  writeln;
  writeln ('3 ===================História====================');
  writeln;
  writeln ('4 ===================Biologia====================');
end;

//Procedimento pro menu de assunto: entreterimento
procedure menu_entreterimento();
begin
  writeln ('=================Entreterimento================');
  writeln;
  writeln ('=================Dificuldade===================');
  writeln;
  writeln ('1 - Fácil');
  writeln;
  writeln ('2 - Intermediário');
  writeln;
  writeln ('3 - Difícil');
  writeln;
end;

//Procedimento pro menu de assunto: matemática
procedure menu_matematica();
begin
  writeln ('==================Matemática===================');
  writeln;
  writeln ('=================Dificuldade===================');
  writeln;
  writeln ('1 - Fácil');
  writeln;
  writeln ('2 - Intermediário');
  writeln;
  writeln ('3 - Difícil');
  writeln;
end;

//Procedimento pro menu de assunto: história
procedure menu_historia();
begin
  writeln ('===================História====================');
  writeln;
  writeln ('=================Dificuldade===================');
  writeln;
  writeln ('1 - Fácil');
  writeln;
  writeln ('2 - Intermediário');
  writeln;
  writeln ('3 - Difícil');
  writeln;
end;

//Procedimento pro menu de assunto: biologia
procedure menu_biologia();
begin
  writeln ('===================Biologia====================');
  writeln;
  writeln ('=================Dificuldade===================');
  writeln;
  writeln ('1 - Fácil');
  writeln;
  writeln ('2 - Intermediário');
  writeln;
  writeln ('3 - Difícil');
  writeln;
  
  readln (opcao_dificuldade);
  clrscr;
  
  case opcao_dificuldade of
    1:
    begin
      writeln ('===================DICA=====================');
      writeln;
      writeln ('Microrganismo usado na fermentação para a fabricação de cerveja e de pães');
      readln (resp);
      if (resp = resposta[1]) then
      begin
        pontos := pontos + 10;
      end
    end;
    
    2:
    begin
      writeln ('===================DICA=====================');
      writeln;
      writeln ('Ramo da zoologia que estuda os insetos');
      readln (resp);
      if (resp = resposta[2]) then
      begin
        pontos := pontos + 25;
      end
    end;
    
    3:
    begin
      writeln ('===================DICA=====================');
      writeln;
      writeln ('Embrião');
      readln (resp);
      if (resp = resposta[4]) then
      begin
        pontos := pontos + 50;
      end
    end; 
  end;
end;

Begin
  
  //Microrganismo usado na fermentação para a fabricação de cerveja e de pães
  resposta[1]:= 'fungo';
  //Ramo da zoologia que estuda os insetos
  resposta[2]:= 'entomologia';
  //Sal mineral presente na coagulação do sangue
  resposta[3]:= 'calcio';
  //Complexo embrionário exclusivo dos mamíferos
  resposta[4]:= 'placenta';
  
  //Chama o procedimento do menu principal
  menu_principal();
  
  //Recebe a opção digitada pelo usuário e limpa a tela
  readln (opcao_menu);
  clrscr;
  
  //Caso ele escolha a primeira opção, começa o jogo
  case opcao_menu of
    1:
    begin
      //Procedimento para o menu de assuntos
      menu_assuntos();
      
      //Recebe a opção digitada pelo usuário e limpa a tela
      readln (opcao_assunto);
      clrscr;
      
      //Caso escolha a primeira opção, vai para o menu de dificuldade das perguntas na área do entreterimento
      if (opcao_assunto = 1) then
      begin
        menu_entreterimento();
      end
      
      //Caso escolha a segunda opção, vai para o menu de dificuldade das perguntas na área da matemática
      else
      if (opcao_assunto = 2) then
      begin
        menu_matematica();
      end
      
      //Caso escolha a terceira opção, vai para o menu de dificuldade das perguntas na área da história
      else
      if (opcao_assunto = 3) then
      begin
        menu_historia();
      end
      
      //Caso escolha a quarta opção, vai para o menu de dificuldades das perguntas na área da biologia
      else
      if (opcao_assunto = 4) then
      begin
        menu_biologia();
      end
    end;
    //Caso escolha a segunda opção no menu principal, abre as instruções
    2:
    begin
      writeln ('======================Instruções==================');
      writeln;
      write ('O objetivo deste jogo é descobrir uma palavra adivinhando suas letras.');
      write ('Após escolher o tema e a dificuldade, o jogador irá escolher uma letra que suspeite fazer parte da palavra.');
      write ('Caso a palavra contenha esta letra, será mostrado em que posição (ões) ela está. Entretanto, caso esta letra não exista na palavra, será desenhada uma parte do corpo do boneco do jogador. ');
      write ('Se todas as 6 partes do corpo do boneco estiverem desenhadas, o jogador perderá.');
    end;
    
    //Caso escolha a terceira opção no menu principal, abre a loja
    3:
    begin
      writeln ('=========================Loja=======================');
    end;
  end;
  
  writeln ('Você tem: ',pontos,' pontos');
  
End.
