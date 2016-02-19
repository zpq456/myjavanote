#Android AsyncTask란?
안드로이드에서 사용하는 UI를 총괄하는 메인쓰레드이며
UI처리 및 Background 작업 등을 하나의 클래스에서 작업이
가능하게 지원해주는 클래스.
따라서 일반쓰레드를 따로 만들고 적절히 핸들링을 해가면서
작업 할 필요가 없다.

![](http://cfile6.uf.tistory.com/image/131B56204B9997C872FBA9)


##Android AsyncTask의 사용법
AsyncTask클래스를 사용할때 지정해야하는 generic type은 각각
다음의 용도로 사용된다.
-Params: background작업 시 필요한 data의 type 지정
-Progress: background 작업 중 진행상황을 표현하는데 사용되는 
data를 위한 type 지정
-Result: background 작업 완료 후 리턴 할 data 의 type 지정
Ex) private class ABC externs AsyncTask<Parans,Progress,Result>{...}
![](http://cfile22.uf.tistory.com/image/143C23054B987FDDB74F04)

AsyncTask클래스는 항상 Subclassing 해서 사용 해야 함.
-(Params)background 작업에 사용할 data의 자료형: String 형
-(Progress)background 작업 진행 표시를 위해 사용할 인자: Integer형
-(Result)background 작업의 결과를 표현할 자료형: Long
-인자를 사용하지 않은 경우 Void Type 으로 지정.
 
AsyncTask는 일반쓰레드와 핸들러를 사용하지 않고 CallBack
매서드만을 이용해서 UI수정이나 Background작업을 진행한다.
-protected void onPreExecute(): Background 작업이 시작되자마자 
UI스레드에서 실행될 코드를 구현해야 함. 
(예. background 작업의 시작을 알리는 text표현, background 
작업을 위한 ProgressBar popup등)
-protected abstract Result doInBackground(Params… params): 
Background에서 수행할 작업을 구현해야 함. execute(…) 메소드에 
입력된 인자들을 전달 받음.
-void onProgressUpdate(Progress... values): publishProgress(…) 
메소드 호출의 callback으로 UI스레드에서 보여지는 background 
작업 진행 상황을 update하도록 구현함. (예. ProgressBar 증가 등)
-void onPostExecute(Result result): doInBackground(…)가 
리턴하는 값을 바탕으로 UI스레드에 background 작업 결과를 
표현하도록 구현 함. (예. background작업을 계산한 복잡한 
산술식에 대한 답을 UI 위젯에 표현함 등)
-void onCancelled(): AsyncTask:cancel(Boolean) 메소드를 
사용해 AsyncTask인스턴스의 background작업을 정지 또는 
실행금지 시켰을 때 실행되는 callback. background작업의 
실행정지에 따른 리소스복구/정리 등이 구현될 수 있다.

또한 AsyncTask 클래스는 background작업의 시작과 진행정보의
UI스레드 표현을 위해 다음과 같은 메소드를 제공한다.
-final AsyncTask<…> execute(Params… params): Background 작업을
 시작한다. 꼭 UI스레드에서 호출하여야 함. 가변인자를 
받아들임으로 임의의 개수의 인자를 전달할 수 있으며, 
인자들은 doInBackground(…) 메소드로 전달된다.
-final void publishProgress(Progress... values): Background 작업
 수행 중 작업의 진행도를 UI 스레드에 전달 함. 
doInBackground(…)메소드 내부에서만 호출.

AsyncTask인서턴스의 상태를 호출하는 매서드
public final AsyncTask.Status getStatus ()

background작업을 정지 또는 시작금지 시키기 위한 매서드
final boolean cancel (boolean matInterruptlfRunning)


AsyncTask를 사용해 background작업을 구현시 꼭 지켜야 하는 사항
-AsyncTask클래스는 항상 subclassing 하여 사용하여야 한다.
-AsyncTask 인스턴스는 항상 UI 스레드에서 생성한다.
-AsyncTask:execute(…) 메소드는 항상 UI 스레드에서 호출한다.
-AsyncTask:execute(…) 메소드는 생성된 AsyncTask 인스턴스 
별로 꼭 한번만 사용 가능하다. 같은 인스턴스가 또 execute(…)를 
실행하면 exception이 발생하며, 이는 AsyncTask:cancel(…) 
메소드에 의해 작업완료 되기 전 취소된 AsyncTask 인스턴스라도 
마찬가지이다. 그럼으로 background 작업이 필요할 때마다 new 
연산자를 이용해 해당 작업에 대한 AsyncTask 인스턴스를 새로 
생성해야 한다.
-AsyncTask의 callback 함수 onPreExecute(), doInBackground(…), 
onProgressUpdate(…), onPostExecute(…)는 직접 호출 하면 
안 된다. (꼭 callback으로만 사용)


