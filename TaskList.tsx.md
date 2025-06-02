"use client";

import React from 'react';
import TaskCard from '@/components/task/TaskCard';

interface Task {
    id: string;
    title: string;
    description: string;
    dueDate: string;
    priority: 'High' | 'Medium' | 'Low';
}

interface TaskListProps {
    tasks: Task[];
}

const TaskList: React.FC<TaskListProps> = ({ tasks }) => {
    return (
        <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
            {tasks.map(task => (
                <TaskCard
                    key={task.id}
                    title={task.title}
                    description={task.description}
                    dueDate={task.dueDate}
                    priority={task.priority}
                />
            ))}
        </div>
    );
};

export default TaskList;
