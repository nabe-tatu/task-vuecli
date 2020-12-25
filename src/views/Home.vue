<template>
    <div class="home">

        <RouterView/>
        <div class="container mt-5">
            <div class="row">
                <div class="col">
                    <div class="input-group mb-3">
                        <input type="text" class="form-control" placeholder="フォルダ" aria-label="Recipient's username" aria-describedby="button-addon2">
                        <button class="btn btn-outline-secondary" type="button" id="button-addon2">追加</button>
                    </div>
                </div>
                <div class="col">
                    <div class="input-group mb-3">
                        <input type="text" class="form-control" placeholder="タスク" aria-label="Recipient's username" aria-describedby="button-addon2">
                        <button class="btn btn-outline-secondary" type="button" id="button-addon2">追加</button>
                    </div>
                </div>
            </div>

            <div class="row">
                <div class="col">
                    <div class="list-group">
                        <!--classにactive aria-current="true" 追加-->
                        <a v-for="folder in folders" :key="folder.id" href="#" class="list-group-item list-group-item-action">
                            {{ folder.folderName }}
                        </a>
                    </div>
                </div>
                <div class="col">
                    <div class="list-group">
                        <!--classにdisabled tabindex="-1" aria-disabled="true 追加-->
                        <a v-for="task in tasks" v-bind:key="task.id" href="#" class="list-group-item list-group-item-action">
                            {{ task.taskName }}
                        </a>
                    </div>
                </div>
            </div>
        </div>


    </div>
</template>

<script>
    // @ is an alias to /src
    //import HelloWorld from '@/components/HelloWorld.vue'

    export default {
        name: 'Home',
        data: function () {
            return {
                folders:[
                    {
                        id:1,
                        folderName:'仕事'
                    },
                    {
                        id:2,
                        folderName:'生活'
                    },
                    {
                        id:3,
                        folderName:'遊び'
                    },
                    {
                        id:4,
                        folderName:'その他'
                    },
                    {
                        id:5,
                        folderName:'aaaaa'
                    },
                ],
                tasks:[
                    {
                        id:1,
                        taskName:'メールチェック'
                    },
                    {
                        id:2,
                        taskName:'打刻'
                    },
                    {
                        id:3,
                        taskName:'実装'
                    },
                    {
                        id:4,
                        taskName:'テスト'
                    },
                    {
                        id:5,
                        taskName:'リリース'
                    },
                    {
                        id:6,
                        taskName:'aaa'
                    },
                ]
            }
        }
    }
</script>
