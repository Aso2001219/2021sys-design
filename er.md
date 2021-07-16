```uml
@startuml
!define MASTER_MARK_COLOR Orange 
!define TRANSACTION_MARK_COLOR DeepSkyBlue

'グラデーションさせる場合 #xx-xx
!define MAIN_ENTITY #MintCream-MistyRose

/'
  デフォルト色を"skinparam class"で設定します。
'/
skinparam class {
    '図の背景
    BackgroundColor Snow
    '図の枠
    BorderColor Black
    'リレーションの色
    ArrowColor Black
}

entity"顧客マスタ" as customer <m_customer>
<<M.MASTER_MARK_COLOR>>{
  + customer_code [PK]
  --
  pass
  name
  address
  tel
  mail
  del_flag
  reg_date
}
  
@enduml
```
