> ### 此文档只是总结常用的组件及参数的使用。具体使用查看[官方文档]([Ant Design - 一套企业级 UI 设计语言和 React 组件库](https://ant.design/index-cn))



## 使用 Ant React

`npm install antd --save`

> 官方已经完美优化了按需引入，所以不需要配置其他



### Table

```react
import {Table} from 'antd'
/*
	属性 columns列的数据  dataSource行的数据
	columns  接收一个数组，数组中是各个对象
		对象中配置项
            title  : 列名
            dataIndex : dataSource中的键名，作用：渲染dataSource中的数据
            key  :  唯一标识
            render : 函数 (_,record){ _ 为dataIndex数据，record为dataSource对象 }
    dataSource 接收一个数组，数据中是对象
    	需要通过key 来做唯一标识
    	其他数据项自拟
*/
function Con(){
    const columns = [
        {
            title: 'Name',
            dataIndex: 'name',
            key: 'name',
            render: (_, record) => {
                console.log(record);
                return <a>{record.name}</a>
            },
        },
        {
            title: 'Age',
            dataIndex: 'age',
            key: 'age',
        },
        {
            title: 'Address',
            dataIndex: 'address',
            key: 'address',
        },
        {
            title: 'Tags',
            key: 'tags',
            dataIndex: 'tags',
            render: (_, {tags}) => (
                <>
                    {tags.map((tag) => {
                        let color = tag.length > 5 ? 'geekblue' : 'green';
                        if (tag === 'loser') {
                            color = 'volcano';
                        }
                        return (
                            <Tag color={color} key={tag}>
                                {tag.toUpperCase()}
                            </Tag>
                        );
                    })}
                </>
            ),
        },
        {
            title: 'Action',
            key: 'action',
            render: (_, record) => (
                <Space size="middle">
                    <a>Invite {record.name}</a>
                    <a>Delete</a>
                </Space>
            ),
        },
    ];
    const data = [
        {
            key: '1',
            name: 'John Brown',
            age: 32,
            address: 'New York No. 1 Lake Park',
            tags: ['nice', 'developer'],
        },
        {
            key: '2',
            name: 'Jim Green',
            age: 42,
            address: 'London No. 1 Lake Park',
            tags: ['loser'],
        },
        {
            key: '3',
            name: 'Joe Black',
            age: 32,
            address: 'Sydney No. 1 Lake Park',
            tags: ['cool', 'teacher'],
        },
    ];
    return (
        <Table columns={columns} dataSource={data}/>
    )
}
```

