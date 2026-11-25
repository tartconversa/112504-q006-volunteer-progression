# 居民主理人成长轨迹与接班风险

活动履历区分被指派角色和已核实的责任。录入日期和生效日期分开。

## 资料

CSV 样例为合成记录，使用 UTF-8，首行为字段名。多值用竖线分隔，空单元格表示来源未填。记录日期和业务生效日期各有含义。

- people.csv 的字段为 person、block、joined、exit。
- practice.csv 的字段为 event、person、episode、type、role、responsibility、observed、confirmed、revision。
- requests.csv 的字段为 slot、type、start、stop、required_roles、state、original_lead。
- staffing.csv 的字段为 record、person、slot、availability、received。
- eligibility.csv 的字段为 type、role、example_qualifier、supervisor。

## 运行资料检查

在项目根目录使用 Python 3.11 或更高版本。依赖仅为标准库。

~~~sh
python3 -m compileall -q tests
python3 -m unittest discover -s tests -v
~~~
