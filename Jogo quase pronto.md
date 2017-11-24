Program Jogo_forca ;

uses

crt;

var
resposta: array[1..12] of string;
pergunta: array[1..12] of string;
opcao_menu, opcao_assunto, opcao_dificuldade, pontos, i, tentativa: integer;
resp, sair, teste: string;

procedure boneco();
begin
  writeln('     /NMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMo        ');
  writeln('     .syyyNMyyyyyyyydMMMMmyyyyyyyyyyyMMMo        ');
  writeln('          hM         :dMMMy.         mMMo        ');
  writeln('          hM           :dMMMy.       mMMo        ');
  writeln('          hM             :dMMMy.     mMMo        ');
  writeln('          hM               :dMMMy.   mMMo        ');
  writeln('      ..` hM                 :dMMMy. mMMo        ');
  writeln('    oNMMMmmM                   :dMMMyNMMo        ');
  writeln('   /MMMMMMMM                     :dMMMMMo        ');
  writeln('   .NMMMMMMMmy:                    :hMMMo        ');
  writeln('    `/hMMMMMMMMd.                    mMMo        ');
  writeln('     :NMMMMMMMMMN-                   mMMo        ');
  writeln('    :MMMMMMMMMNMMm                   mMMo        ');
  writeln('   `NMMyNMMMMM/MMM/                  mMMo        ');
  writeln('   oMMN`NMMMMM:dMMy                  mMMo        ');
  writeln('   yMMd NMMMMM:sMMm                  mMMo        ');
  writeln('   +MMy NMMMMM--dmy                  mMMo        ');
  writeln('    ``  NMM MMM`                      NMMs       ');
  writeln('       `MMM MMM.                     yMMMM/      ');
  writeln('       :MMM MMM-                    sMMMMMM/     ');
  writeln('       sMMN MMM+                   oMMMMMMMM/    ');
  writeln('       hMMy mMMs                  /MMMMMMNMMM:   ');
  writeln('       yMM/ hMMs                 :MMMomMMosMMM:  ');
end;

procedure boneco_cabeca();
begin
  writeln('     /NMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMo        ');
  writeln('     .syyyNMyyyyyyyydMMMMmyyyyyyyyyyyMMMo        ');
  writeln('          hM         :dMMMy.         mMMo        ');
  writeln('          hM           :dMMMy.       mMMo        ');
  writeln('          hM             :dMMMy.     mMMo        ');
  writeln('          hM               :dMMMy.   mMMo        ');
  writeln('      ..` hM                 :dMMMy. mMMo        ');
  writeln('    oNMMMmmM                   :dMMMyNMMo        ');
  writeln('   /MMMMMMMM                     :dMMMMMo        ');
  writeln('   .NMMMMMMMmy                     :hMMMo        ');
  writeln('                                     mMMo        ');
  writeln('                                     mMMo        ');
  writeln('                                     mMMo        ');
  writeln('                                     mMMo        ');
  writeln('                                     mMMo        ');
  writeln('                                     mMMo        ');
  writeln('                                     mMMo        ');
  writeln('                                     NMMs        ');
  writeln('                                    yMMMM/       ');
  writeln('                                   sMMMMMM/      ');
  writeln('                                  oMMMMMMMM/     ');
  writeln('                                 /MMMMMMNMMM:    ');
  writeln('                                :MMMomMMosMMM:   ');
end;

procedure boneco_corpo();
begin
  writeln('     /NMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMo        ');
  writeln('     .syyyNMyyyyyyyydMMMMmyyyyyyyyyyyMMMo        ');
  writeln('          hM         :dMMMy.         mMMo        ');
  writeln('          hM           :dMMMy.       mMMo        ');
  writeln('          hM             :dMMMy.     mMMo        ');
  writeln('          hM               :dMMMy.   mMMo        ');
  writeln('      ..` hM                 :dMMMy. mMMo        ');
  writeln('    oNMMMmmM                   :dMMMyNMMo        ');
  writeln('   /MMMMMMMM                     :dMMMMMo        ');
  writeln('   .NMMMMMMMmy:                    :hMMMo        ');
  writeln('    `/hMMMMMMMMd.                    mMMo        ');
  writeln('     :NMMMMMMMMMN-                   mMMo        ');
  writeln('    :MMMMMMMMMNMMm                   mMMo        ');
  writeln('       yNMMMMM/                      mMMo        ');
  writeln('       `NMMMMM:                      mMMo        ');
  writeln('        NMMMMM:                      mMMo        ');
  writeln('        NMMMMM-                      mMMo        ');
  writeln('                                     NMMs        ');
  writeln('                                    yMMMM/       ');
  writeln('                                   sMMMMMM/      ');
  writeln('                                  oMMMMMMMM/     ');
  writeln('                                 /MMMMMMNMMM:    ');
  writeln('                                :MMMomMMosMMM:   ');
end;

procedure boneco_braco1();
begin
  writeln('     /NMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMo        ');
  writeln('     .syyyNMyyyyyyyydMMMMmyyyyyyyyyyyMMMo        ');
  writeln('          hM         :dMMMy.         mMMo        ');
  writeln('          hM           :dMMMy.       mMMo        ');
  writeln('          hM             :dMMMy.     mMMo        ');
  writeln('          hM               :dMMMy.   mMMo        ');
  writeln('      ..` hM                 :dMMMy. mMMo        ');
  writeln('    oNMMMmmM                   :dMMMyNMMo        ');
  writeln('   /MMMMMMMM                     :dMMMMMo        ');
  writeln('   .NMMMMMMMmy:                    :hMMMo        ');
  writeln('    `/hMMMMMMMMd.                    mMMo        ');
  writeln('     :NMMMMMMMMMN-                   mMMo        ');
  writeln('    :MMMMMMMMMNMMm                   mMMo        ');
  writeln('   `NMMyNMMMMM/                      mMMo        ');
  writeln('   oMMN`NMMMMM:                      mMMo        ');
  writeln('   yMMd NMMMMM:                      mMMo        ');
  writeln('   +MMy NMMMMM-                      mMMo        ');
  writeln('    ``                               NMMs        ');
  writeln('                                    yMMMM/       ');
  writeln('                                   sMMMMMM/      ');
  writeln('                                  oMMMMMMMM/     ');
  writeln('                                 /MMMMMMNMMM:    ');
  writeln('                                :MMMomMMosMMM:   ');
end;

procedure boneco_braco2();
begin
  writeln('     /NMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMo        ');
  writeln('     .syyyNMyyyyyyyydMMMMmyyyyyyyyyyyMMMo        ');
  writeln('          hM         :dMMMy.         mMMo        ');
  writeln('          hM           :dMMMy.       mMMo        ');
  writeln('          hM             :dMMMy.     mMMo        ');
  writeln('          hM               :dMMMy.   mMMo        ');
  writeln('      ..` hM                 :dMMMy. mMMo        ');
  writeln('    oNMMMmmM                   :dMMMyNMMo        ');
  writeln('   /MMMMMMMM                     :dMMMMMo        ');
  writeln('   .NMMMMMMMmy:                    :hMMMo        ');
  writeln('    `/hMMMMMMMMd.                    mMMo        ');
  writeln('     :NMMMMMMMMMN-                   mMMo        ');
  writeln('    :MMMMMMMMMNMMm                   mMMo        ');
  writeln('   `NMMyNMMMMM/MMM/                  mMMo        ');
  writeln('   oMMN`NMMMMM:dMMy                  mMMo        ');
  writeln('   yMMd NMMMMM:sMMm                  mMMo        ');
  writeln('   +MMy NMMMMM--dmy                  mMMo        ');
  writeln('    ``                               NMMs        ');
  writeln('                                    yMMMM/       ');
  writeln('                                   sMMMMMM/      ');
  writeln('                                  oMMMMMMMM/     ');
  writeln('                                 /MMMMMMNMMM:    ');
  writeln('                                :MMMomMMosMMM:   ');
end;

procedure boneco_perna1();
begin
  writeln('     /NMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMo        ');
  writeln('     .syyyNMyyyyyyyydMMMMmyyyyyyyyyyyMMMo        ');
  writeln('          hM         :dMMMy.         mMMo        ');
  writeln('          hM           :dMMMy.       mMMo        ');
  writeln('          hM             :dMMMy.     mMMo        ');
  writeln('          hM               :dMMMy.   mMMo        ');
  writeln('      ..` hM                 :dMMMy. mMMo        ');
  writeln('    oNMMMmmM                   :dMMMyNMMo        ');
  writeln('   /MMMMMMMM                     :dMMMMMo        ');
  writeln('   .NMMMMMMMmy:                    :hMMMo        ');
  writeln('    `/hMMMMMMMMd.                    mMMo        ');
  writeln('     :NMMMMMMMMMN-                   mMMo        ');
  writeln('    :MMMMMMMMMNMMm                   mMMo        ');
  writeln('   `NMMyNMMMMM/MMM/                  mMMo        ');
  writeln('   oMMN`NMMMMM:dMMy                  mMMo        ');
  writeln('   yMMd NMMMMM:sMMm                  mMMo        ');
  writeln('   +MMy NMMMMM--dmy                  mMMo        ');
  writeln('    ``  NMM                           NMMs       ');
  writeln('       `MMM                          yMMMM/      ');
  writeln('       :MMM                         sMMMMMM/     ');
  writeln('       sMMN                        oMMMMMMMM/    ');
  writeln('       hMMy                       /MMMMMMNMMM:   ');
  writeln('       yMM/                      :MMMomMMosMMM:  ');
end;

procedure condicional();
begin
  repeat
    begin
      writeln ('Digite a resposta');
      readln (resp);
      clrscr;
      if (resp <> resposta[opcao_dificuldade]) then
      begin
        tentativa := tentativa + 1
      end
      else
      if (resp = resposta[opcao_dificuldade]) then
      begin
        writeln ('Você acertou');
        pontos := pontos + 10;
        break
      end;
      
      if (tentativa = 1) then
      begin
        boneco_cabeca();
        writeln ('Digite a resposta');
        readln (resp);
        if (resp = resposta[opcao_dificuldade]) then
        begin
          clrscr;
          boneco_cabeca();
          writeln ('Você acertou');
          pontos := pontos + 10;
          break
        end
        else
        if (resp <> resposta[opcao_dificuldade]) then
        begin
          tentativa := tentativa + 1
        end;
      end;
      
      if (tentativa = 2) then
      begin
        clrscr;
        boneco_corpo();
        writeln ('Digite a resposta');
        readln (resp);
        if (resp = resposta[opcao_dificuldade]) then
        begin
          clrscr;
          boneco_corpo();
          writeln ('Você acertou');
          pontos := pontos + 10;
          break
        end
        else
        if (resp <> resposta[opcao_dificuldade]) then
        begin
          tentativa := tentativa + 1
        end;
      end;
      
      if (tentativa = 3) then
      begin
        clrscr;
        boneco_braco1();
        writeln ('Digite a resposta');
        readln (resp);
        if (resp = resposta[opcao_dificuldade]) then
        begin
          clrscr;
          boneco_braco1();
          writeln ('Você acertou');
          pontos := pontos + 10;
          break
        end
        else
        if (resp <> resposta[opcao_dificuldade]) then
        begin
          tentativa := tentativa + 1
        end;
      end;
      
      if (tentativa = 4) then
      begin
        clrscr;
        boneco_braco2();
        writeln ('Digite a resposta');
        readln (resp);
        if (resp = resposta[opcao_dificuldade]) then
        begin
          clrscr;
          boneco_braco2();
          writeln ('Você acertou');
          pontos := pontos + 10;
          break
        end
        else
        if (resp <> resposta[opcao_dificuldade]) then
        begin
          tentativa := tentativa + 1
        end;
      end;
      
      if (tentativa = 5) then
      begin
        clrscr;
        boneco_perna1();
        writeln ('Digite a resposta');
        readln (resp);
        if (resp = resposta[opcao_dificuldade]) then
        begin
          clrscr;
          boneco_perna1();
          writeln ('Você acertou');
          pontos := pontos + 10;
          break
        end
        else
        if (resp <> resposta[opcao_dificuldade]) then
        begin
          tentativa := tentativa + 1
        end;
      end;
      
      if (tentativa = 6) then
      begin
        clrscr;
        boneco();
        writeln ('Você perdeu');
        tentativa := tentativa + 1
      end;
    end;
  until (tentativa > 0);
end;

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

//Procedimento pro menu de assunto: lógica
procedure menu_logica();
begin
  writeln ('====================Lógica=====================');
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
      if (opcao_dificuldade = 1) then
      begin
        condicional();
      end;
    end;
    
    2:
    begin
      writeln ('===================DICA=====================');
      writeln;
      writeln ('Ramo da zoologia que estuda os insetos');
      if (opcao_dificuldade = 2) then
      begin
        condicional();
      end;
    end;
    
    3:
    begin
      writeln ('===================DICA=====================');
      writeln;
      writeln ('Embrião - 8 LETRAS');
      if (opcao_dificuldade = 3) then
      begin
        condicional();
      end;
    end;
  end;
end;

Begin
  pergunta[1]:= 'Microrganismo usado na fermentação para a fabricação de cerveja e de pães';
  resposta[1]:= 'fungo';
  
  pergunta[2]:= 'Ramo da zoologia que estuda os insetos';
  resposta[2]:= 'entomologia';
  
  pergunta[3]:= 'Complexo embrionário exclusivo dos mamíferos';
  resposta[3]:= 'placenta';
  
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
      
      //Caso escolha a segunda opção, vai para o menu de dificuldade das perguntas na área de lógica
      else
      if (opcao_assunto = 2) then
      begin
        menu_logica();
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
