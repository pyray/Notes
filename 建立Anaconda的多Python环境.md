# ����Anaconda�Ķ�Python����

## 1. ���conda�µ�Python����

��װanaconda��������·���������ڿ���̨�������������Լ�����еĻ�����

    conda info -e
    
��ʱӦ�ÿ�������conda������ЩPython�������������װAnaconda��ĳһ���汾�������ֻ��һ����root��

## 2. ��conda������һ��Python����

    conda create --name mypy3 python=3  #����һ������Ϊmypy3��ʹ��Python3.x�汾�Ļ�����conda�������������ذ�װ���µ�Python3.x��

## 3. ���Python����

    activate mypy3                      #��windowsϵͳ�м������mypy3�����������Ubuntuϵͳ����Ϊ source activate mypy3
    python -V                           #���û�����Python�İ汾��Ӧ������Ҫ��3.x�档��ʱ�������ģʽ������python��������Ӧ�汾��python�༭��
    deactivate mypy3                    #�˳�mypy3��������ʱ�ص�Ĭ�ϵ�Python�汾������У�
    
## 4. ��Jupyter notebook�����Ӹû�������ѡ��
    
    activate mypy3
    conda install ipykernel             #����Ӧ�����а�װipykernel�����ڸ������Ƕ����ģ���ÿһ��������Ҫ�ֱ�װ
    python -m ipykernel install --user  #��jupyter notebook �����Ӹû���ѡ������Ubuntu�£���д��mypy3 -m ipykernel install --user
    deactivate mypy3                    #�˳�mypy3������ͬ������Ubuntu�£���Ҫ��ǰ������source
    
�ظ��������裬�������Ӳ�ͬ�汾��Python������

Ȼ�������Jupyter notebook��ѡ���½���ͬ�汾Python��notebook�ļ���Ҳ�����������ǽ��к����л���
    