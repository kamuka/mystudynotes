SDRAM  
�ο�
[���ʵ�blog](http://blog.csdn.net/mr_raptor/article/details/6555786)  
[S3C2440��SDRAM�ĵ�ַ���߷���](http://www.360doc.com/content/11/0914/17/7715138_148241178.shtml)

���ͣ�
- ʲô��Ƭѡ

- mini2440��SDRAM�Ĵ�С��ô����
һƬSDRAM��������32MB��������16b * 4M * 4bank,���������߼�bank��ɣ�ÿ��bank����4M����Ԫ��ÿ����Ԫ��16��bit����2���ֽڣ���ÿ���߼�Bank��������8MB��һƬSDRAM��������Ϊ(2B * 4M) * 4bank = 32MB��
 
- Ϊ��SDRAM�ĵ�ַ����A0~A12��ֻ��13���߾͹��ˡ�
SDRAM�ڲ���һ���洢���С����԰��������һ�����񡣺ͱ���ļ���ԭ��һ������ָ���У���ָ���У��Ϳ���׼ȷ�ҵ�����Ҫ�Ĵ洢��Ԫ����������Ϊ�߼�BANK��Ŀǰ��SDRAM��������4��BANK��Ѱַ�����̾�����ָ��BANK��ַ����ָ���е�ַ�����ָ���е�ַ�������SDRAM��Ѱַԭ�����鿴HY57V561620F�����ϣ����SDRAM��13���е�ַ��(RA0-RA12),9���е�ַ��(CA0-CA8), 2��BANKѡ����(BA0-BA1)������ÿ���߼�Bank�ϵ�4M���ڴ浥Ԫ��4M=2^2*2^20=2^22����������13��*9�и���Ԫһһ��Ӧ��ͬʱ����SDRAM�ĵ�ַ�����Ǹ��õ�,�ڶ�дSDRAM�洢��Ԫʱ�����������ǽ���д��ÿ����Ԫ�ĵ�ַ���������뵽SDRAMоƬ�е���/�е�ַ����������һ�������е�ַ���ڶ��������е�ַ�����Կ��Ը���A0-A12��ֻҪ��13����ַ�߾��㹻�ˡ�

- Ϊ��S3C2440��SDRAM֮������ʱ��SDRAM��A0�Ǻ�S3C2440��ADDR2��
��Ϊ��mini2440�ϣ����˼·�ǰ���Ƭ32MB��SDRAM������������CPU��ADDR2~ADDR14��13����ַ�ߣ��������߷ֿ�����һƬSDRAMʹ��DATA0~DATA15���ڶ�ƬSDRAMʹ��DATA16~DATA31������SDRAM��CSƬѡ����CPU��nGCS6���ӡ��ﵽ��Ч�����ǵ�CPUָ��һ��SDRAM�ĵ�ַʱ��ͨ��ͬʱѡ����ƬSDRAM��������������ͬʱȡ����ƬSDRAM��������Ԫ����4���ֽڵ����ݡ����仰˵��CPU�ϵĵ�ַ��λ��SDRAM�ϵĵ�ַ��λ��1��4�ĸ��������������ʱ������CPU�ĵ���λ��������Ǻ���CPU��ADDR0��ADDR1����CPU��ADDR2��ʼ��SDRAM��A0���ӡ�

- ldrbָ�������ʵ��ȡ�ֵĲ����ֽ�
���ǲ���Ҫ���ģ�ȡ�����ֽڵĲ�������S3C2440�ڲ��ĵ�SDRAM������ʵ�֣��������Ա������SDRAM�����������DQMx�ܽţ�Ӱ��SDRAM��LDQM��UDQM�����β���Ҫ���ֽڡ�

