<template>
    <header class="site-header">
        <div class="header-inner">
            <div class="brand">KKBOX</div>
            <nav class="main-nav">
                <a href="#" @click.prevent="emit('open-login')">
                    訂閱方案
                </a>

                <a href="#" @click.prevent="emit('open-login')">
                    支援平台
                </a>

                <a href="#" @click.prevent="emit('open-login')">
                    音樂趨勢
                </a>

                <a href="#" @click.prevent="emit('open-login')">
                    會員服務
                </a>

                <a href="#" @click.prevent="emit('open-login')">
                    關於 KKBOX
                </a>
            </nav>
            <div class="header-actions">
                <button
                    class="icon"
                    @click="emit('open-login')"
                >
                🔍
                </button>

                <button
                    class="btn outline download"
                    @click="emit('open-login')"
                >
                下載
                </button>
        </div>
      </div>
    </header>
</template>

<script setup>
const emit = defineEmits(['open-login'])
</script>

<style scoped>
    .site-header{
        background: var(--header);
        color:#fff;
        position:sticky;
        top:0;
        z-index:30;
        width:100%;
    }

    .header-inner{
        max-width:1180px;
        margin:0 auto;

        display:flex;
        align-items:center;
        justify-content:space-between;

        padding:12px 18px;
    }

    .brand {
        color: var(--accent);
        font-weight: 700
    }

    .main-nav a {
        color: #d9d9d9;
        text-decoration: none;
        margin: 0 10px;
        font-size: 13px
    }

    .header-actions {
        display: flex;
        gap: 8px;
        align-items: center
    }

    .header-actions .download {
        background: transparent;
        color: #fff;
        border: 1px solid rgba(255, 255, 255, 0.06);
        padding: 6px 10px;
        border-radius: 4px
    }

    .site-header {
        background: var(--header);
        color: #fff;
        position: sticky;
        top: 0;
        z-index: 30
    }

    .header-inner {
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 12px 18px
    }

    .brand {
        color: var(--accent);
        font-weight: 700;
        letter-spacing: 0.6px
    }

    .header-actions .download {
        background: transparent;
        color: #fff;
        border: 1px solid rgba(255, 255, 255, 0.06);
        padding: 6px 10px;
        border-radius: 4px
    }

    .site-header.scrolled {
        box-shadow: 0 2px 8px rgba(0, 0, 0, 0.2)
    }
</style>