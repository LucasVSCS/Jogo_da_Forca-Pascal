# Jogo da Forca - Pascal
Program Jogo_forca ;

var
resposta: array[1..4] of string;
opcao_menu, opcao_assunto, opcao_dificuldade, pontos: integer;
resp: string;

Begin
  
  //Microrganismo usado na fermentação para a fabricação de cerveja e de pães
  resposta[1]:= 'Fungo';
  //Ramo da zoologia que estuda os insetos
  resposta[2]:= 'Entomologia';
  //Sal mineral presente na coagulação do sangue
  resposta[3]:= 'Calcio';
  //Complexo embrionário exclusivo dos mamíferos
  resposta[4]:= 'Placenta';
  
  
  writeln ('=================Jogo da Forca===================');
  writeln;
  writeln ('1 ===================Começar=====================');
  writeln;
  writeln ('2 ==================Instruções===================');
  writeln;
  writeln ('3 ====================Loja=======================');
  writeln;
  
  
  readln (opcao_menu);
  clrscr;
  
  
  if (opcao_menu = 1) then
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
    writeln;
    
    readln (opcao_assunto);
    clrscr;
    
    if (opcao_assunto = 1) then
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
    end
    
    
    else
    if (opcao_assunto = 2) then
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
    end
    
    else
    if (opcao_assunto = 3) then
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
    end
    
    else
    if (opcao_assunto = 4) then
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
      
      if (opcao_dificuldade = 1) then
      begin
        writeln ('===================DICA=====================');
        writeln;
        writeln ('Microrganismo usado na fermentação para a fabricação de cerveja e de pães');
        readln (resp);
        if (resp = resposta[1]) then
        begin
          pontos := pontos + 10;
        end
      end
      else
      if (opcao_dificuldade = 2) then
      begin
        writeln ('===================DICA=====================');
        writeln;
        writeln ('Ramo da zoologia que estuda os insetos');
        readln (resp);
        if (resp = resposta[2]) then
        begin
          pontos := pontos + 25;
        end
      end
      else
      if (opcao_dificuldade = 3) then
      begin
        writeln ('===================DICA=====================');
        writeln;
        writeln ('Embrião');
        readln (resp);
        if (resp = resposta[4]) then
        begin
          pontos := pontos + 50;
        end
      end
    end;
  end;
  
  writeln (pontos)
End.
