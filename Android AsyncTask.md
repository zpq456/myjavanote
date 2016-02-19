#Android AsyncTask��?
�ȵ���̵忡�� ����ϴ� UI�� �Ѱ��ϴ� ���ξ������̸�
UIó�� �� Background �۾� ���� �ϳ��� Ŭ�������� �۾���
�����ϰ� �������ִ� Ŭ����.
���� �Ϲݾ����带 ���� ����� ������ �ڵ鸵�� �ذ��鼭
�۾� �� �ʿ䰡 ����.

![](http://cfile6.uf.tistory.com/image/131B56204B9997C872FBA9)


##Android AsyncTask�� ����
AsyncTaskŬ������ ����Ҷ� �����ؾ��ϴ� generic type�� ����
������ �뵵�� ���ȴ�.
-Params: background�۾� �� �ʿ��� data�� type ����
-Progress: background �۾� �� �����Ȳ�� ǥ���ϴµ� ���Ǵ� 
data�� ���� type ����
-Result: background �۾� �Ϸ� �� ���� �� data �� type ����
Ex) private class ABC externs AsyncTask<Parans,Progress,Result>{...}
![](http://cfile22.uf.tistory.com/image/143C23054B987FDDB74F04)

AsyncTaskŬ������ �׻� Subclassing �ؼ� ��� �ؾ� ��.
-(Params)background �۾��� ����� data�� �ڷ���: String ��
-(Progress)background �۾� ���� ǥ�ø� ���� ����� ����: Integer��
-(Result)background �۾��� ����� ǥ���� �ڷ���: Long
-���ڸ� ������� ���� ��� Void Type ���� ����.
 
AsyncTask�� �Ϲݾ������ �ڵ鷯�� ������� �ʰ� CallBack
�ż��常�� �̿��ؼ� UI�����̳� Background�۾��� �����Ѵ�.
-protected void onPreExecute(): Background �۾��� ���۵��ڸ��� 
UI�����忡�� ����� �ڵ带 �����ؾ� ��. 
(��. background �۾��� ������ �˸��� textǥ��, background 
�۾��� ���� ProgressBar popup��)
-protected abstract Result doInBackground(Params�� params): 
Background���� ������ �۾��� �����ؾ� ��. execute(��) �޼ҵ忡 
�Էµ� ���ڵ��� ���� ����.
-void onProgressUpdate(Progress... values): publishProgress(��) 
�޼ҵ� ȣ���� callback���� UI�����忡�� �������� background 
�۾� ���� ��Ȳ�� update�ϵ��� ������. (��. ProgressBar ���� ��)
-void onPostExecute(Result result): doInBackground(��)�� 
�����ϴ� ���� �������� UI�����忡 background �۾� ����� 
ǥ���ϵ��� ���� ��. (��. background�۾��� ����� ������ 
����Ŀ� ���� ���� UI ������ ǥ���� ��)
-void onCancelled(): AsyncTask:cancel(Boolean) �޼ҵ带 
����� AsyncTask�ν��Ͻ��� background�۾��� ���� �Ǵ� 
������� ������ �� ����Ǵ� callback. background�۾��� 
���������� ���� ���ҽ�����/���� ���� ������ �� �ִ�.

���� AsyncTask Ŭ������ background�۾��� ���۰� ����������
UI������ ǥ���� ���� ������ ���� �޼ҵ带 �����Ѵ�.
-final AsyncTask<��> execute(Params�� params): Background �۾���
 �����Ѵ�. �� UI�����忡�� ȣ���Ͽ��� ��. �������ڸ� 
�޾Ƶ������� ������ ������ ���ڸ� ������ �� ������, 
���ڵ��� doInBackground(��) �޼ҵ�� ���޵ȴ�.
-final void publishProgress(Progress... values): Background �۾�
 ���� �� �۾��� ���൵�� UI �����忡 ���� ��. 
doInBackground(��)�޼ҵ� ���ο����� ȣ��.

AsyncTask�μ��Ͻ��� ���¸� ȣ���ϴ� �ż���
public final AsyncTask.Status getStatus ()

background�۾��� ���� �Ǵ� ���۱��� ��Ű�� ���� �ż���
final boolean cancel (boolean matInterruptlfRunning)


AsyncTask�� ����� background�۾��� ������ �� ���Ѿ� �ϴ� ����
-AsyncTaskŬ������ �׻� subclassing �Ͽ� ����Ͽ��� �Ѵ�.
-AsyncTask �ν��Ͻ��� �׻� UI �����忡�� �����Ѵ�.
-AsyncTask:execute(��) �޼ҵ�� �׻� UI �����忡�� ȣ���Ѵ�.
-AsyncTask:execute(��) �޼ҵ�� ������ AsyncTask �ν��Ͻ� 
���� �� �ѹ��� ��� �����ϴ�. ���� �ν��Ͻ��� �� execute(��)�� 
�����ϸ� exception�� �߻��ϸ�, �̴� AsyncTask:cancel(��) 
�޼ҵ忡 ���� �۾��Ϸ� �Ǳ� �� ��ҵ� AsyncTask �ν��Ͻ��� 
���������̴�. �׷����� background �۾��� �ʿ��� ������ new 
�����ڸ� �̿��� �ش� �۾��� ���� AsyncTask �ν��Ͻ��� ���� 
�����ؾ� �Ѵ�.
-AsyncTask�� callback �Լ� onPreExecute(), doInBackground(��), 
onProgressUpdate(��), onPostExecute(��)�� ���� ȣ�� �ϸ� 
�� �ȴ�. (�� callback���θ� ���)


