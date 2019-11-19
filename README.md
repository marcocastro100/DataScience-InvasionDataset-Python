# DataScience-InvasionDataset-Python
Data PreProcessing, Exploratory Analisys, Statistic Analisys and Machine_Learning from a dataset of invasion KDD-99 using Python

O software para detectar invasões de rede protege uma rede de computadores contra usuários não autorizados, incluindo talvez pessoas de dentro da empresa. A tarefa de aprendizagem do detector de intrusões é construir um modelo preditivo (ou seja, um classificador) capaz de distinguir entre conexões "ruins", chamadas intrusões ou ataques e conexões normais "boas".
 
O Programa de Avaliação de Detecção de Intrusão DARPA de 1998 foi preparado e gerenciado pelo MIT Lincoln Labs. O objetivo era pesquisar e avaliar pesquisas em detecção de intrusões. Foi fornecido um conjunto padrão de dados a serem auditados, que inclui uma ampla variedade de intrusões simuladas em um ambiente de rede militar. O concurso de detecção de intrusão do KDD de 1999 usa uma versão deste conjunto de dados.

ATAQUES Presentes no Dataset

DOS: negação de serviço;\
R2L: acesso não autorizado de uma máquina remota;\
U2R: acesso não autorizado a privilégios locais de superusuário (raiz);\
Probe: vigilância e outras sondagens;

FEATURES do Dataset:\

DURATION: duração (número de segundos) da conexão.\
PROTOCOL_TYPE: tipo do protocolo,  como: tcp, udp, etc.\
SERVICE: serviço rodando na rede destino, por exemplo, http, telnet etc.\
SRC_BYTES: número de bytes de dados da origem ao destino.\
DST_BYTES: número de bytes de dados do destino à origem.\
FLAG: status normal ou de erro da conexão.\
LAND: 1 se a conexão for de/para o mesmo host/porta; 0 caso contrário\
WRONG_FRAGMENT: número de fragmentos “errados”' \
URGENT: número de pacotes urgentes \
HOT: número de “hot indicators”'\
NUM_FAILED_LOGINS: número de tentativas com falha no login\
LOGGED_IN: 1 se logado com sucesso; 0 caso contrário\
NUM_COMPROMISED: número de condições comprometidas \
ROOT_SHELL: 1 se o shell raiz for obtido; 0 caso contrário\
SU_ATTEMPTED: 1 se a tentativa do comando “su root”' foi executada; 0 caso contrário\
NUM_ROOT: número de acessos “root”'\
NUM_FILE_CREATIONS: número de operações de criação de arquivo\
NUM_SHELLS: número de solicitações de shell\
NUM_ACCESS_FILES: número de operações nos arquivos de controle de acesso\
 NUM_OUTBOUND_CMDS: número de comandos de saída em uma sessão ftp\
 IS_HOT_LOGIN: 1 se o login pertencer à lista “hot”, 0 caso contrário \
IS_GUEST_LOGIN: 1 se o login for um log de convidado; 0 caso contrário\
COUNT: número de conexões com o mesmo host que a conexão atual nos últimos dois segundos\
NOTE: Os seguintes recursos se referem a essas conexões no mesmo host.\
SERROR_RATE: % de conexões com erros “SYN” \
RERROR_RATE: % de conexões com erros de “REJ”\
SAME_SRV_RATE: % de conexões com o mesmo serviço\
DIFF_SRV_RATE: % de conexões com diferentes serviços\
SRV_COUNT: número de conexões com o mesmo serviço que a conexão atual nos últimos dois segundos\
NOTE: Os recursos a seguir se referem a conexões de mesmo serviço.\
SRV_SERROR_RATE: % de conexões com erros “SYN” \
SRV_RERROR_RATE: % de conexões que possuem erros de “REJ”'\
SRV_DIFF_HOST_RATE: % de conexões com diferentes hosts\
CLASS: Tipo de conexão (AtaqueType Vs Normal)

FLAG'S do DataSet

'S0: Tentativa de conexão vista, sem resposta.\
'S1: Conexão estabelecida, não finalizada.\
'SF: Estabelecimento e rescisão normais. Observe que este é o
	'mesmo símbolo do estado S1. Você pode diferenciar os dois porque
	'para S1, não haverá contagens de bytes no resumo, enquanto
 	'para SF haverá.\
'REJ: Tentativa de conexão rejeitada.\
‘S2:  Conexão estabelecida e tentativa de fechamento pelo originador vista
	'(mas nenhuma resposta do respondente).\
'S3: Conexão estabelecida e tentativa próxima por respondedor vista
	'(mas nenhuma resposta do remetente).\
‘RSTO: conexão estabelecida, originador abortado (enviado um RST).\
'RSTR: O respondente enviou um RST.\
'RSTOS0: Originator enviou um SYN seguido por um RST, nunca vimos um
	'SYN-ACK do atendedor.\
'RSTRH: O respondente enviou um SYN ACK seguido por um RST, nunca vimos um SYN
	'do originador (suposto).\
'SH: Originator enviou um SYN seguido por um FIN, nunca vimos um SYN ACK\
	'do atendedor (portanto, a conexão foi "metade" aberta).\
'O SHR: Responder enviou um SYN ACK seguido por um FIN, nunca vimos um SYN
	'do remetente.\
'OTH: Nenhum SYN visto, apenas tráfego intermediário (uma “conexão parcial” que
'não foi fechado mais tarde).\
